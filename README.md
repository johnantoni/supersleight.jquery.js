# supersleight.jquery.js

You apply it to a section of the page like this:

$('#content').supersleight();

Of course, if you wanted to fix PNGs for the entire page, you can just apply it to the body element. For all sorts of reasons, it’s better to be specific if you can.

$('body').supersleight();

This can be safely reapplied after importing a chunk of HTML via an Ajax request (something I end up doing a lot), and it uses jQuery’s browser detection to only apply it to the appropriate versions of IE, so it’s safe to deploy for everything, or to include inside some Conditional Comments as you prefer.

As always, the script requires the path to a transparent GIF shim image. By default, and almost by tradition with this script, that’s x.gif, but you can specify any image you like:

$('body').supersleight({shim: '/img/transparent.gif'});

Other possible configuration values are imgs and backgrounds (both boolean, default true) to tell the script which PNGs to fix up, and apply_positioning (boolean, default true) to tell the script not to try and fix up some of the bugs around unclickable links. (See the 24ways article for more info on that).

http://allinthehead.com/retro/338/supersleight-jquery-plugin
http://24ways.org/2007/supersleight-transparent-png-in-ie6

another way is to save images as 8-bit PNGs, which should provide a workable solution without need of the plugin although may appear a little fuzzy
