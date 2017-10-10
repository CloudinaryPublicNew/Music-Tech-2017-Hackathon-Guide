# Video transcoding, resizing, cropping and manipulating made easy

![](https://cloudinary-res.cloudinary.com/image/upload/c_fill,w_470/dpr_2.0/video_transcoding_manipulation.jpg)
By Meir Feinberg
Sep 02, 2015


Videos are becoming more prolific with people having the capability to capture videos with a wide variety of cameras, including smartphone cameras that are available almost everywhere. Web and mobile applications that display videos online can be faced with a challenge when the videos are created or uploaded from different devices and in various formats, and then need to be delivered in **a multitude of resolutions and aspect ratios to various web browsers, laptops and all kinds of mobile devices** in HTML5 web friendly video formats. 

On top of that, the videos may need to be further manipulated to fit the graphic design of the web application, whether that entails cropping, resizing, rotating, trimming, adding overlays, or even applying filters and various effects.

Developing and then supporting the backend required to transform videos from hi-res originals to HTML5 web friendly video formats that fit the graphic design of your application is a non-trivial technical process that requires considerable computational power. There are also many advanced tuning properties related to video encoding in the trade off between visual quality and file size, and doing this correctly can save a lot of bandwidth and load videos faster. Many developers spend considerable time building in-house solutions to support online videos.

Cloudinary offers a solution to all your development needs with:

* No need to install any complex software - **all video processing takes place in the cloud**, together with an Interactive Media Library for browsing through your media files and SDKs for all popular web and mobile development frameworks for easy integration with HTML5 sites and mobile apps.
* No need to learn how to fine tune video creation - all the best practices are already automatically applied with conversion to all formats **(MP4, WebM, OGV, FLV)** for optimized viewing on all web browsers and mobile devices, improving your website's loading speed while reducing your bandwidth requirements and IT costs.
* No need to write complex code for video processing - all code is already available as a service with a URL based API for video transcoding and manipulation.
* No need to deploy servers for video processing - it's a hosted solution.
* No need to pre-generate all video manipulations - video transformations are done on the fly, streamed via a CDN.

## Cloud-based video manipulation

Manipulating videos to fit the graphic design of the web application doesn't need to be complicated and hard to implement even if the video needs to be delivered in different sizes, formats and resolutions while supporting all the different web browsers, laptops and mobile devices. Cloudinary's rich set of video manipulation capabilities include: [resizing and cropping][138], [rotating][139], modifying [quality][140], adjusting [video codec settings][141], controlling [bit rate][142], [video trimming][143], [thumbnail generation][144], [conversion to animated GIF][145], adding [text][146], [image][147] and [video][148] overlays, [special effects][149] and lots [more][150]. Videos are delivered using dynamic URLs with on-the-fly transcoding and real-time manipulation while streaming the video content via a worldwide CDN with streaming support for the best performance.

The following are some examples of manipulating a video called `funny_dog` that was uploaded to Cloudinary. 

[URL][151][Ruby][151][PHP][151][Python][151][Node.js][151][Java][151][JS][151][jQuery][151][React][151][Angular][151][.Net][151][Android][151][All][151]

URL:

[`https://res.cloudinary.com/demo/video/upload/funny_dog.mp4][152]`

Ruby:
    
    
    cl_video_tag("funny_dog")

PHP:
    
    
    cl_video_tag("funny_dog")

Python:
    
    
    CloudinaryVideo("funny_dog").video()

Node.js:
    
    
    cloudinary.video("funny_dog")

Java:
    
    
    cloudinary.url().videoTag("funny_dog")

JS:
    
    
    cl.videoTag('funny_dog').toHtml();

jQuery:
    
    
    $.cloudinary.video("funny_dog")

React:
    
    
    

Angular:
    
    
    
    
    

.Net:
    
    
    cloudinary.Api.UrlVideoUp.BuildVideoTag("funny_dog")

Android:
    
    
    MediaManager.get().url().resourceType("video").generate("funny_dog.mp4")

### [Video resizing and cropping][153]

Resize the video to a width of 200 pixels and a height of 150 pixels using the `fill` cropping mode and focusing on the bottom of the video in the case that only a portion of the video is used:

[URL][154][Ruby][154][PHP][154][Python][154][Node.js][154][Java][154][JS][154][jQuery][154][React][154][Angular][154][.Net][154][Android][154][All][154]

URL:

[`https://res.cloudinary.com/demo/video/upload/w_200,h_150,c_fill,g_south/funny_dog.mp4][155]`

Ruby:
    
    
    cl_video_tag("funny_dog", :width=>200, :height=>150, :gravity=>"south", :crop=>"fill")

PHP:
    
    
    cl_video_tag("funny_dog", array("width"=>200, "height"=>150, "gravity"=>"south", "crop"=>"fill"))

Python:
    
    
    CloudinaryVideo("funny_dog").video(width=200, height=150, gravity="south", crop="fill")

Node.js:
    
    
    cloudinary.video("funny_dog", {width: 200, height: 150, gravity: "south", crop: "fill"})

Java:
    
    
    cloudinary.url().transformation(new Transformation().width(200).height(150).gravity("south").crop("fill")).videoTag("funny_dog")

JS:
    
    
    cl.videoTag('funny_dog', {width: 200, height: 150, gravity: "south", crop: "fill"}).toHtml();

jQuery:
    
    
    $.cloudinary.video("funny_dog", {width: 200, height: 150, gravity: "south", crop: "fill"})

React:
    
    
    

Angular:
    
    
    
      
      
    

.Net:
    
    
    cloudinary.Api.UrlVideoUp.Transform(new Transformation().Width(200).Height(150).Gravity("south").Crop("fill")).BuildVideoTag("funny_dog")

Android:
    
    
    MediaManager.get().url().transformation(new Transformation().width(200).height(150).gravity("south").crop("fill")).resourceType("video").generate("funny_dog.mp4")

Resize the video to a width of 300 pixels and a height of 200 pixels using the `pad` cropping mode and use a blue background in the case that the video needs padding:

[URL][156][Ruby][156][PHP][156][Python][156][Node.js][156][Java][156][JS][156][jQuery][156][React][156][Angular][156][.Net][156][Android][156][All][156]

URL:

[`https://res.cloudinary.com/demo/video/upload/w_300,h_200,c_pad,b_rgb:0e4167/funny_dog.mp4][157]`

Ruby:
    
    
    cl_video_tag("funny_dog", :width=>300, :height=>200, :background=>"#0e4167", :crop=>"pad")

PHP:
    
    
    cl_video_tag("funny_dog", array("width"=>300, "height"=>200, "background"=>"#0e4167", "crop"=>"pad"))

Python:
    
    
    CloudinaryVideo("funny_dog").video(width=300, height=200, background="#0e4167", crop="pad")

Node.js:
    
    
    cloudinary.video("funny_dog", {width: 300, height: 200, background: "#0e4167", crop: "pad"})

Java:
    
    
    cloudinary.url().transformation(new Transformation().width(300).height(200).background("#0e4167").crop("pad")).videoTag("funny_dog")

JS:
    
    
    cl.videoTag('funny_dog', {width: 300, height: 200, background: "#0e4167", crop: "pad"}).toHtml();

jQuery:
    
    
    $.cloudinary.video("funny_dog", {width: 300, height: 200, background: "#0e4167", crop: "pad"})

React:
    
    
    

Angular:
    
    
    
      
      
    

.Net:
    
    
    cloudinary.Api.UrlVideoUp.Transform(new Transformation().Width(300).Height(200).Background("#0e4167").Crop("pad")).BuildVideoTag("funny_dog")

Android:
    
    
    MediaManager.get().url().transformation(new Transformation().width(300).height(200).background("#0e4167").crop("pad")).resourceType("video").generate("funny_dog.mp4")

### [Video overlays, trimming, transcoding and more][158]

Scale the width to 300 pixels, the height to 200 pixels, set the quality to 40 and add an overlay saying "Funny Dog" in Roboto 30px white text starting at the 3 second mark and 10 pixels from the bottom of the video:

[URL][159][Ruby][159][PHP][159][Python][159][Node.js][159][Java][159][JS][159][jQuery][159][React][159][Angular][159][.Net][159][Android][159][All][159]

URL:

[`https://res.cloudinary.com/demo/video/upload/w_300,h_200,q_40/l_text:Roboto_30px_bold:Funny Dog,co_white,g_south,y_10,so_3/funny_dog.mp4][160]`

Ruby:
    
    
    cl_video_tag("funny_dog", :transformation=>[
      {:width=>300, :height=>200, :quality=>40, :crop=>"scale"},
      {:overlay=>"text:Roboto_30px_bold:Funny%20Dog", :color=>"white", :gravity=>"south", :y=>10, :start_offset=>"3"}
      ])

PHP:
    
    
    cl_video_tag("funny_dog", array("transformation"=>array(
      array("width"=>300, "height"=>200, "quality"=>40, "crop"=>"scale"),
      array("overlay"=>"text:Roboto_30px_bold:Funny%20Dog", "color"=>"white", "gravity"=>"south", "y"=>10, "start_offset"=>"3")
      )))

Python:
    
    
    CloudinaryVideo("funny_dog").video(transformation=[
      {"width": 300, "height": 200, "quality": 40, "crop": "scale"},
      {"overlay": "text:Roboto_30px_bold:Funny%20Dog", "color": "white", "gravity": "south", "y": 10, "start_offset": "3"}
      ])

Node.js:
    
    
    cloudinary.video("funny_dog", {transformation: [
      {width: 300, height: 200, quality: 40, crop: "scale"},
      {overlay: "text:Roboto_30px_bold:Funny%20Dog", color: "white", gravity: "south", y: 10, start_offset: "3"}
      ]})

Java:
    
    
    cloudinary.url().transformation(new Transformation()
      .width(300).height(200).quality(40).crop("scale").chain()
      .overlay("text:Roboto_30px_bold:Funny%20Dog").color("white").gravity("south").y(10).startOffset("3")).videoTag("funny_dog")

JS:
    
    
    cl.videoTag('funny_dog', {transformation: [
      {width: 300, height: 200, quality: 40, crop: "scale"},
      {overlay: "text:Roboto_30px_bold:Funny%20Dog", color: "white", gravity: "south", y: 10, start_offset: "3"}
      ]}).toHtml();

jQuery:
    
    
    $.cloudinary.video("funny_dog", {transformation: [
      {width: 300, height: 200, quality: 40, crop: "scale"},
      {overlay: "text:Roboto_30px_bold:Funny%20Dog", color: "white", gravity: "south", y: 10, start_offset: "3"}
      ]})

React:
    
    
    

Angular:
    
    
    
      
      
      
      
    

.Net:
    
    
    cloudinary.Api.UrlVideoUp.Transform(new Transformation()
      .Width(300).Height(200).Quality(40).Crop("scale").Chain()
      .Overlay("text:Roboto_30px_bold:Funny%20Dog").Color("white").Gravity("south").Y(10).StartOffset("3")).BuildVideoTag("funny_dog")

Android:
    
    
    MediaManager.get().url().transformation(new Transformation()
      .width(300).height(200).quality(40).crop("scale").chain()
      .overlay("text:Roboto_30px_bold:Funny%20Dog").color("white").gravity("south").y(10).startOffset("3")).resourceType("video").generate("funny_dog.mp4")

Transcode the video to the `webm` format and apply the best codec settings for web viewing with the `vc_auto` parameter, add the `cloudinary_icon` image overlay with a width of 160 pixels and 10 pixels from the northeast corner with a brightness of 200% and an opacity of 70%, and adjust the total width to 350 pixels and the height to 150 pixels while padding with a blue background:

[URL][161][Ruby][161][PHP][161][Python][161][Node.js][161][Java][161][JS][161][jQuery][161][React][161][Angular][161][.Net][161][Android][161][All][161]

URL:

[`https://res.cloudinary.com/demo/video/upload/vc_auto/l_cloudinary_icon,g_north_east,e_brightness:200,o_70,x_10,y_10,w_160/w_350,h_150,c_pad,b_rgb:0e4167/funny_dog.webm][162]`

Ruby:
    
    
    cl_video_tag("funny_dog", :transformation=>[
      {:video_codec=>"auto"},
      {:overlay=>"cloudinary_icon", :gravity=>"north_east", :effect=>"brightness:200", :opacity=>70, :x=>10, :y=>10, :width=>160},
      {:width=>350, :height=>150, :background=>"#0e4167", :crop=>"pad"}
      ])

PHP:
    
    
    cl_video_tag("funny_dog", array("transformation"=>array(
      array("video_codec"=>"auto"),
      array("overlay"=>"cloudinary_icon", "gravity"=>"north_east", "effect"=>"brightness:200", "opacity"=>70, "x"=>10, "y"=>10, "width"=>160),
      array("width"=>350, "height"=>150, "background"=>"#0e4167", "crop"=>"pad")
      )))

Python:
    
    
    CloudinaryVideo("funny_dog").video(transformation=[
      {"video_codec": "auto"},
      {"overlay": "cloudinary_icon", "gravity": "north_east", "effect": "brightness:200", "opacity": 70, "x": 10, "y": 10, "width": 160},
      {"width": 350, "height": 150, "background": "#0e4167", "crop": "pad"}
      ])

Node.js:
    
    
    cloudinary.video("funny_dog", {transformation: [
      {video_codec: "auto"},
      {overlay: "cloudinary_icon", gravity: "north_east", effect: "brightness:200", opacity: 70, x: 10, y: 10, width: 160},
      {width: 350, height: 150, background: "#0e4167", crop: "pad"}
      ]})

Java:
    
    
    cloudinary.url().transformation(new Transformation()
      .videoCodec("auto").chain()
      .overlay("cloudinary_icon").gravity("north_east").effect("brightness:200").opacity(70).x(10).y(10).width(160).chain()
      .width(350).height(150).background("#0e4167").crop("pad")).videoTag("funny_dog")

JS:
    
    
    cl.videoTag('funny_dog', {transformation: [
      {video_codec: "auto"},
      {overlay: "cloudinary_icon", gravity: "north_east", effect: "brightness:200", opacity: 70, x: 10, y: 10, width: 160},
      {width: 350, height: 150, background: "#0e4167", crop: "pad"}
      ]}).toHtml();

jQuery:
    
    
    $.cloudinary.video("funny_dog", {transformation: [
      {video_codec: "auto"},
      {overlay: "cloudinary_icon", gravity: "north_east", effect: "brightness:200", opacity: 70, x: 10, y: 10, width: 160},
      {width: 350, height: 150, background: "#0e4167", crop: "pad"}
      ]})

React:
    
    
    

Angular:
    
    
    
      
      
      
      
      
      
    

.Net:
    
    
    cloudinary.Api.UrlVideoUp.Transform(new Transformation()
      .VideoCodec("auto").Chain()
      .Overlay("cloudinary_icon").Gravity("north_east").Effect("brightness:200").Opacity(70).X(10).Y(10).Width(160).Chain()
      .Width(350).Height(150).Background("#0e4167").Crop("pad")).BuildVideoTag("funny_dog")

Android:
    
    
    MediaManager.get().url().transformation(new Transformation()
      .videoCodec("auto").chain()
      .overlay("cloudinary_icon").gravity("north_east").effect("brightness:200").opacity(70).x(10).y(10).width(160).chain()
      .width(350).height(150).background("#0e4167").crop("pad")).resourceType("video").generate("funny_dog.webm")

There are plenty of additional video and image manipulation options that you can choose from, we have only shown a few here to give a small taste of how easy it is to manipulate your videos. See our [video documentation][30] for more details and examples.

## [Creating an image thumbnail from a video][163]

You can also easily create image thumbnails of any frame in a video and then apply any of Cloudinary's [image transformations][23] to the result. For example, to create an image thumbnail of the frame at 1 second in the `funny_dog` video in JPG format, scaled to a width of 250 pixels and a height of 150 pixels:

[URL][164][Ruby][164][PHP][164][Python][164][Node.js][164][Java][164][JS][164][jQuery][164][React][164][Angular][164][.Net][164][Android][164][All][164]

URL:

[`https://res.cloudinary.com/demo/video/upload/w_250,h_150,c_scale,so_1/funny_dog.jpg][165]`

Ruby:
    
    
    cl_image_tag("funny_dog.jpg", :width=>250, :height=>150, :start_offset=>"1", :crop=>"scale", :resource_type=>"video")

PHP:
    
    
    cl_image_tag("funny_dog.jpg", array("width"=>250, "height"=>150, "start_offset"=>"1", "crop"=>"scale", "resource_type"=>"video"))

Python:
    
    
    CloudinaryVideo("funny_dog.jpg").image(width=250, height=150, start_offset="1", crop="scale")

Node.js:
    
    
    cloudinary.image("funny_dog.jpg", {width: 250, height: 150, start_offset: "1", crop: "scale", resource_type: "video"})

Java:
    
    
    cloudinary.url().transformation(new Transformation().width(250).height(150).startOffset("1").crop("scale")).resourceType("video").imageTag("funny_dog.jpg")

JS:
    
    
    cl.videoTag('funny_dog.jpg', {width: 250, height: 150, start_offset: "1", crop: "scale"}).toHtml();

jQuery:
    
    
    $.cloudinary.image("funny_dog.jpg", {width: 250, height: 150, start_offset: "1", crop: "scale", resource_type: "video"})

React:
    
    
    

Angular:
    
    
    
      
      
    

.Net:
    
    
    cloudinary.Api.UrlVideoUp.Transform(new Transformation().Width(250).Height(150).StartOffset("1").Crop("scale")).BuildImageTag("funny_dog.jpg")

Android:
    
    
    MediaManager.get().url().transformation(new Transformation().width(250).height(150).startOffset("1").crop("scale")).resourceType("video").generate("funny_dog.jpg")

![jpg created from funny_dog.mp4 scaled to 250x150][166]

To create a circular 300x300 sharpened image thumbnail in JPG format of the frame at the 15% mark of the `funny_dog` video, and then adding the `cloudinary_icon` image overlay with a north gravity and resizing to a width of 50% of the total image with 40% opacity:

[URL][167][Ruby][167][PHP][167][Python][167][Node.js][167][Java][167][JS][167][jQuery][167][React][167][Angular][167][.Net][167][Android][167][All][167]

URL:

[`https://res.cloudinary.com/demo/video/upload/w_300,h_300,c_fill,r_max,e_sharpen,so_15p/l_cloudinary_icon,w_0.5,fl_relative,o_40,g_north/funny_dog.jpg][168]`

Ruby:
    
    
    cl_image_tag("funny_dog.jpg", :resource_type=>"video", :transformation=>[
      {:width=>300, :height=>300, :radius=>"max", :effect=>"sharpen", :start_offset=>"15p", :crop=>"fill"},
      {:overlay=>"cloudinary_icon", :width=>0.5, :flags=>"relative", :opacity=>40, :gravity=>"north"}
      ])

PHP:
    
    
    cl_image_tag("funny_dog.jpg", array("resource_type"=>"video", "transformation"=>array(
      array("width"=>300, "height"=>300, "radius"=>"max", "effect"=>"sharpen", "start_offset"=>"15p", "crop"=>"fill"),
      array("overlay"=>"cloudinary_icon", "width"=>0.5, "flags"=>"relative", "opacity"=>40, "gravity"=>"north")
      )))

Python:
    
    
    CloudinaryVideo("funny_dog.jpg").image(transformation=[
      {"width": 300, "height": 300, "radius": "max", "effect": "sharpen", "start_offset": "15p", "crop": "fill"},
      {"overlay": "cloudinary_icon", "width": 0.5, "flags": "relative", "opacity": 40, "gravity": "north"}
      ])

Node.js:
    
    
    cloudinary.image("funny_dog.jpg", {resource_type: "video", transformation: [
      {width: 300, height: 300, radius: "max", effect: "sharpen", start_offset: "15p", crop: "fill"},
      {overlay: "cloudinary_icon", width: "0.5", flags: "relative", opacity: 40, gravity: "north"}
      ]})

Java:
    
    
    cloudinary.url().transformation(new Transformation()
      .width(300).height(300).radius("max").effect("sharpen").startOffset("15p").crop("fill").chain()
      .overlay("cloudinary_icon").width(0.5).flags("relative").opacity(40).gravity("north")).resourceType("video").imageTag("funny_dog.jpg")

JS:
    
    
    cl.videoTag('funny_dog.jpg', {transformation: [
      {width: 300, height: 300, radius: "max", effect: "sharpen", start_offset: "15p", crop: "fill"},
      {overlay: "cloudinary_icon", width: "0.5", flags: "relative", opacity: 40, gravity: "north"}
      ]}).toHtml();

jQuery:
    
    
    $.cloudinary.image("funny_dog.jpg", {resource_type: "video", transformation: [
      {width: 300, height: 300, radius: "max", effect: "sharpen", start_offset: "15p", crop: "fill"},
      {overlay: "cloudinary_icon", width: "0.5", flags: "relative", opacity: 40, gravity: "north"}
      ]})

React:
    
    
    

Angular:
    
    
    
      
      
      
      
    

.Net:
    
    
    cloudinary.Api.UrlVideoUp.Transform(new Transformation()
      .Width(300).Height(300).Radius("max").Effect("sharpen").StartOffset("15p").Crop("fill").Chain()
      .Overlay("cloudinary_icon").Width(0.5).Flags("relative").Opacity(40).Gravity("north")).BuildImageTag("funny_dog.jpg")

Android:
    
    
    MediaManager.get().url().transformation(new Transformation()
      .width(300).height(300).radius("max").effect("sharpen").startOffset("15p").crop("fill").chain()
      .overlay("cloudinary_icon").width(0.5).flags("relative").opacity(40).gravity("north")).resourceType("video").generate("funny_dog.jpg")

![Sharpened, rounded jpg created from the frame at 15% of funny_dog.mp4 filled to 300x300 with an overlay][169]

## [Summary][170]

Video uploading and delivery has become more and more popular and developers face a significant challenge handling these video files for embedding in their web and mobile apps while maintaining complex clusters to handle video uploading and transcoding. Cloudinary eliminates all the R&D work involved, and with a single line of code videos are uploaded to the cloud, and then with dynamic URLs, videos are automatically converted to all required video formats and manipulated to fit the graphic design of web applications and the various devices and resolutions.

The video manipulation features are available to all our free and paid plans. If you don't have a Cloudinary account, you are welcome to [sign up to our free account][123] and try it out.