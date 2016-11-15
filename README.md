"# Random Img Frm Flickr" 


Platform: Javascript,Ajax,Html

<pre>
var keyword = "bueatiful";

    $(document).ready(function(){

        $.getJSON("http://api.flickr.com/services/feeds/photos_public.gne?jsoncallback=?",
        {
            tags: keyword,
            tagmode: "any",
            format: "json"
        },
        function(data) {
 
            var rnd = Math.floor(Math.random() * data.items.length);

            var image_src = data.items[rnd]['media']['m'].replace("_m", "_b");

          $('body').css('background-image', "url('" + image_src + "') ");
    			//$('body').css('background-size', "cover");
    			$('body').css('background-repeat', "no-repeat ");
    			//$('body').css('background-position', "center center");	              
    
    
        });

    });
</pre>


