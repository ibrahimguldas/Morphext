Morphext
========

A simple jQuery rotating / carousel plugin for text phrases powered by [Animate.css][animatecss] and inspired by a Dota 2 hero, Morphling. It is more succinctly described by [Softpedia](http://webscripts.softpedia.com/script/Text-Management/Text-Tools/Morphext-82875.html) as:

> A jQuery plugin for creating text-based carousels, rotating small or large pieces of text one after the other, just like a slider does with images... This can be a great tool for displaying catch phrases, mission statements, tag lines, and so on.


[Website][website]

[Demo][demo]


Install
-------

Download from the [project page][downloads].

Install with [Bower][bower]: `bower install --save Morphext`


Usage
-----

1. Import the latest Animate.css and jQuery library into your HTML.

2. Import `morphext.css` and include `morphext.min.js` in your HTML document.

3. Encapsulate your rotating phrases in an element and separate each phrase with a comma or a separator of your choice:

        I am a <span id="js-rotating">So Simple, Very Doge, Much Wow, Such Cool</span> Text Rotator

4. Trigger the plugin by calling Morphext() on the element containing the rotating phrases:

        $("#js-rotating").Morphext();

A demo titled `index.html` is included in this repository. Open it to see the end-result.


Options
-------

Morphext exposes the following options to alter the behaviour of the plugin:

- __animation:__ The [in] animation type. Refer to [Animate.css][animatecss] for a list of available animations. _Default: "bounceIn" (string)_
- __separator:__ An array of phrases to rotate are created based on this separator. Change it if you wish to separate the phrases differently (e.g. So Simple | Very Doge | Much Wow | Such Cool). _Default: "," (string)_
- __speed:__ The delay between the changing of each phrase in milliseconds. _Default: 2000 (int)_

They may be used like so:

        $("#js-rotating").Morphext({
                animation: "fadeIn", // Overrides default "bounceIn"
                separator: "|", // Overrides default ","
                speed: 3000 // Overrides default 2000
        });

The plugin relies heavily on [Animate.css][animatecss] for its [smooth, high performance animations](http://www.html5rocks.com/en/tutorials/speed/high-performance-animations/) to transition between each phrase. Thus, the default animation speed (different from the interval between each phrase as described above) may be altered via CSS:

        #yourElement, .yourClass {
                /* Overrides Animate.css 1s duration */
                -vendor-animation-duration: 3s;
        }


Prerequisites
-------------
- [jQuery][jquery]
- [Animate.css][animatecss]


License
-------
Morphext is licensed under the MIT license [(http://ian.mit-license.org/)](http://ian.mit-license.org/).

  [website]: http://morphext.fyianlai.com/
  [demo]: http://www.enactuslse.co.uk/
  [downloads]: //github.com/MrSaints/Morphext/releases
  
  [bower]: http://bower.io/
  [jquery]: //www.jquery.com/
  [animatecss]: //daneden.github.io/animate.css/
