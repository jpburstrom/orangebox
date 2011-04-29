=Documentation=

==jQuery Plugin Installation==

To install the jQuery plugin, unpack the zip file and place the orangebox folder on your server. You must reference the style sheet and the Javascript file in the head section of your web page along with jQuery 1.5.1 or higher. Assuming you put this folder at the root of your site and that the folder is named "orangebox", it might look like:

<script src="http://code.jquery.com/jquery-1.5.1.min.js"></script> <script type="text/javascript" src="orangebox/js/orangebox.min.js"></script> <link rel="stylesheet" href="orangebox/css/orangebox.css" type="text/css" />

==Plugin Usage==

OrangeBox uses the rel="lightbox" tag on an anchor (<a>).

===Images:===
Create a hyperlink to an image and add rel="lightbox" to the anchor: <a href="/image.jpg" rel="lightbox">link</a>

===QuickTime:===
Create a hyperlink to a QuickTime file and add the width and height to the href: <a href="/quicktime.mov?width=440&height=200" rel="lightbox">link</a>

===Flash:===
Create a hyperlink to the SWF file add the width and height to the href: <a href="/flashfile.swf?width=440&height=200" rel="lightbox">link</a>

===Inline Content:===
Create an anchor link with href="#inlineContent": <a href="#inlineContent" rel="lightbox">link</a> <div id="inlineContent" style="display:none">Inline Content Here</div>

===iFrame Content:===
Create a hyperlink to the URL and add "?iframe" to the href: <a href="http://google.com?iframe" rel="lightbox">link</a>

===YouTube and Vimeo:===
Create a hyperlink to the YouTube/Vimeo video: <a href="http://www.youtube.com/watch?v=tVvVQc3O01U" rel="lightbox">link</a>

===Item Groups:===
To group items, add the group name between square brackets to the rel: rel="lightbox[groupName]".

===Hidden Item Groups:===
To group items without creating individual hyperlinks, create an un-ordered list. Give the <ul> id="ob_gallery". Each content item must go in a <li> with an id="URL", title="title", and class="groupName". You can then hide the list with CSS: <ul id="ob_gallery" style="display:none"> <li id="images/image1.jpg" class="groupName" title="title"></li> </ul>

===Inline OrangeBox Links:===
To link to other modal content from an Inline Content modal window, create a hyperlink and use rel="lightboxlink". If the linked content belongs to a group, the navigation will be available. <a href="/image.jpg" rel="lightboxlink">link</a>

==Plugin Options==
To set options in OrangeBox, you can either directly edit orangebox.min.js or for an easier option, add an inline script to your head section after declaring the OrangeBox script:
 <script type="text/javascript" src="/orangebox/js/orangebox.min.js"></script> <script type="text/javascript"> ob_showDots = false; ob_overlayOpacity = .7; ob_fileNotFound_Message = "Can't Find File!"; </script>  ===Variables:===

variable
  type
  default

ob_showDots
  true/false
  true
ob_showNav
  true/false
  false
ob_showClose
  true/false
  true
ob_showTitle
  true/false
  true
ob_keyboardNavigation
  true/false
  true
ob_fadeInTime
  milliseconds
  200
ob_fadeOutTime
  milliseconds
  200
ob_preloaderDelay
  milliseconds
  600
ob_contentBorderWidth
  pixels
  4
ob_contentMinHeight
  pixels
  100
ob_contentMinWidth
  pixels
  200
ob_imageBorderWidth
  pixels
  1
ob_overlayOpacity
  percent
  0.9
ob_maxVideoHeight
  0-1: percent, 1+: pixels
  390
ob_maxVideoWidth
  0-1: percent, 1+: pixels
  640
ob_maxImageHeight
0-1: percent, 1+: pixels
0.75
ob_maxImageWidth
  0-1: percent, 1+: pixels
  0.75
ob_inlineWidth
  0-1: percent, 1+: pixels
  0.50
ob_inlineHeight
  0-1: percent, 1+: pixels
  0
ob_iframeWidth
  0-1: percent, 1+: pixels
  0.75
ob_iframeHeight
  0-1: percent, 1+: pixels
  0.75
ob_unsupportedMedia_Message
  text
  "Unsupported Media"
ob_fileNotFound_Message
  text
  "File Not Found"
