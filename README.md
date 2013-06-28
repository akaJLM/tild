tild - tiny front end framework
===============================

Resume
------

**A simple front end framework - more a starter point then a real front-end framework (also it's a Alpha version, only a small part tested yet)**

Currently compatible with IE9+, Chrome, Firefox, Opera, Safari

Under going test + minimal fix (like grid) for IE6, IE7, IE8.

I lost all my files yesterday, I rebuild this idea rapidely this morning and it's only an incomplete Alpha version - also nothing (or only a very small part) already tested yet because I lost also a lot of search on some css hack for all classes (to work fine with each other), I lost some of my proper effects (now it's safe here, also if it's an incomplete Alpha version).

css browser align: normalize.css v1.1.2 by http://necolas.github.io/normalize.css/

The grid structure is very simple
---------------------------------

All is in pourcent (already as possible) 

remark: currently, some css hack was lost when I lost all my files and it's already necessary to made some search on some css hack and (re)fix it (the .box-* in use with in-* and out-*) and also fix the group-h. The first time on my latest files, the float technic worked fine (also with the class sep in group-h) but now it's necessary to re-build and re-test some things.

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

The objective: Each class is only a css hack capable to work correctly with each other (more freedom on the design e.g. .btn design, design of stacked elements, etc...). If the css is not a hack, it's something like an effect, a color, ... (already matched with a class name with (-?)fx-, (-?)color- like .bg-color, etc...). 

If starting with fx-* is not a friendly class name for the autocompletion and the developer (viewable in the auto completion list = auto learn), we can start with a "family" starter-name e.g. .bg-color, .bg-fx-something, ...

Each class must be autocompletion friendly, developer friendly (its name) and aligned with its most valuable "family" name if it's necessary for the autocompletion.

A concept of "Airiness" is introduced
-------------------------------------

This concept can be placed in the middle of this front end framework with the two default classes: .layout AND .grid.

The first idea was to create a js file to manage some dynamic css part generated directly in the dom before /head. this idea was abandonned (not usefull for a few css generated in real usage). Now it's more a "css starter point" for any project more then a "real front end framework" because this part is now include directly in tild.ext.css and can be modifiable (!update - rename this file with the name of the project).

We cannot disturb also the .layout class reserved to the most popular part for a designer (big header element, big nav, big section, big footer element or an entire particular page layout).

javascript usage
----------------

If you need to use javascript in your project, create an empty class prefixed "js-*" (cross-browser) or use data-js="your-event" (modern-browser only) or if you have a complex app your can divided by "brick" data-js="brickname-your-event" or data-js-brickname="your-event" (just idea - was tested).

Leave id already "free" for the back end developer / integrator / wai-ria architect / ... .

Two group for fx
----------------

One group integrated in the CSS file when the effect is not likely to interfere with the user experience (UX) when a browser don't support this effect. Like blur, shake, etc...

The others - not integrated here (leave to the discretion/choice of the developer of the final app) because it's hardeness to introduce multiple style and it's a heavy task for a very small part of a site where this part is too dependent of the general design and designer, also for the footprint this kind of things are not introduced in tild. Like a complex slider for a home page with some elements in position absolute, cheating z-index, multiple files types, multiples tabs, etc... (not included here because you have also a large choice of wheels already build on the web). 

Maybe in a near future a very simple and responsive (ultra small footprint) slider and only based on css3 hack can be introduced.

TO FIX
------

- .group-h > .sep
- .in-*.box-*.out-*

TO ADD
------

- one simple class (small series) to create easily a slider (CSS3 only, no-js except ie6 to 8 to fix it) with a ultra small footprint
