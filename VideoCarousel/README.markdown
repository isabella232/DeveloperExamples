<h2>Video Carousel</h2>

This code was originally implemented for <a href="http://www.syngforhaiti.dk">syngforhaiti.dk</a>, a Danish video site raising money of the victim of the Haiti earthquake in January 2010. The site displays a video element and a photo element -- both importing content via <a href="http://community.23video.com/help/Developer_JS">the Visualplatform JavaScript/JSON API</a> and displaying thumbnails as they are imported. (<a href="/23/DeveloperExamples/blob/master/VideoCarousel/screenshot-carousel.png">See screenshot</a>)

With regard to 23 Video and Visualplatform, this example demonstrates how to...
<ul>
<li>Retrieve data from different video sites using the JSON API, using the callback method.</li>
<li>Parsing the data and using it to build DOM/HTML in the client browser.</li>
<li>Generating an embed code for 23 Video from a video's unique ID.</li>
</ul>


<h2>Code: Displaying carousel and opening videos in a lightbox</h2>
    <link rel="stylesheet" type="text/css" href="videocarousel.css" />

    <div id="videoBadge"></div>
    <div style="clear:left"></div>
      
    <script>
      var videobadge = {
        containerName:'videoBadge',
        domain:'www.syngforhaiti.dk',
        size:300,
        player_id:'',
        player_width:'640',
        player_height:'360',
        params:[]
      };
    </script>
    <script src="videocarousel.js"></script>

You can limit the imported items by modifying the <tt>params</tt> property. For example, to limit to everything tagged "music" in the channel with id "12345":
    params:['tag', 'music', 'album_id', '12345']

<h2>Code: Displaying carousel and open up the 23 Video page on click</h2>
    <link rel="stylesheet" type="text/css" href="videocarousel.css" />

    <div id="videoBadge"></div>
    <div style="clear:left"></div>
      
    <script>
      var videobadge = {
        containerName:'videoBadge',
        domain:'www.syngforhaiti.dk',
        size:300,
        onclick:function(o){location.href='http://www.syngforhaiti.dk' + this.one;}
      };
    </script>
    <script src="videocarousel.js"></script>
