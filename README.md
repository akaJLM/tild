tild - minimal front end framework
==================================

Resume
------

**A simple front end framework - more a starter point then a real front-end framework (also it's a Alpha idea, nothing tested yet)**

Currently compatible with IE9+, Chrome, Firefox, Opera, Safari

I lost all my files yesterday, I rebuild this idea rapidely this morning and it's only an incomplete Alpha idea - also nothing already tested yet because I lost also a lot of search on some css hack for all classes (to work fine with each other), I lost some of my proper effects (now it's safe here, also if it's an incomplete Alpha idea).

Reset: normalize.css v1.1.2 by http://necolas.github.io/normalize.css/

IE6, IE7, IE8 media-queries support by https://github.com/scottjehl/Respond/

The grid structure is very simple
---------------------------------

All is in pourcent (already as possible) 

remark: currently, some css hack was lost and it's already necessary to made some search on css hack and (re)fix it (the .box-* in use with in-* and out-*)

<pre>
            .in-* (implied "inset" = padding)
            =\=======/=
            ==\=====/==
   .pre-*   ===.box-*==   .post-*
            ==/=====\==
            =/=======\=


            .out-* (implied "outset" = margin)
          \             / 
           \           /
            ===========
            ===========
   .pre-*   ===.box-*==   .post-*
            ===========
            ===========
           /           \
          /             \
</pre>

Something -* in the grid scheme is only something in % or something developer/autocompletion friendly (a comprehensive name).

The only one difference between .layout and .grid (the two possible "main parent class" of .box-*) is .layout have a clear status automatically.

.layout is more attempt in some case (or for simply create a more readable html+class structure). 

remark: Nothing tested yet, also .layout class can be evolve.

Some rules
----------

Only left, top, right, bottom, center, auto - and maybe some other (few) elements - can be minified (first-letter) in a class name (.something-l, .something-t, .something-r, .something-b, .something-c, .something-a) - already as possible (!ambiguous).

Only class name like effect, text, background, inset, outset, ... - can be minified (a comprehensive value) like fx, txt, bg, in, out, ...

The objective: Each class is only a css hack capable to work correctly with each other (more freedom on the design e.g. .btn design, design of stacked elements, etc...). If the css is not a hack, it's something like an effect, a color, ... (already matched with a class name with (-?)fx-, (-?)color- like .bg-color, etc...). If starting with fx- is not a friendly class name for the autocompletion or for the developer, we can start with a "family" starter-name e.g. .bg-color, .bg-fx-something, ...

Each class must be autocompletion friendly, developer friendly (its name) and aligned with its most valuable "family" name if it's necessary for autocompletion.

A concept of "Airiness" is introduced
-------------------------------------

This concept can be placed in the middle of this front end framework with the two default classes: .layout AND .grid.

The first idea was to create a js file to manage some dynamic css part generated directly in the dom. this idea was abandonned (not usefull for a few css generated in real usage). Now it's more a "css starter point" for any project more then "real front end framework" because this part is now include directly in the css and can be modifiable (!update).

We cannot disturb also the .layout class reserved to the most popular part for a designer (big header element, big nav, big section, big footer element or an entire particular page layout).

javascript usage
----------------

If you need to use javascript, create an empty class prefixed "js-your-dom-manipulation-class" (cross-browser) or use data-js="your-event" (modern-browser only) or if you have a complex app your can divided by "brick" data-js="brickname-your-event" or data-js-brickname="your-event" (just idea - was tested).

Leave id already "free" for the back end developer / integrator / wai-ria architect / ... .

Two group for fx
----------------

One group integrated in the CSS file when the effect is not likely to interfere with the user experience (UX) when a browser don't support this effect. Like blur, shake, etc...

The others - not integrated here (leave to the discretion/choice of the developer of the final app). Like a slider effect for a home page with some elements in position absolute, cheating z-index, etc... (not included here).