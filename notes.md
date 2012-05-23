Notes
=====

05.13.2012
----------

Trying out LESS for CSS - wanted syntax highlighting in Notepad++, and found
this link: [How to enable syntax highlighting for LESS in 
Notepad++](http://thingsilearned2day.wordpress.com/2011/07/07/how-to-enable-syntax-highlighting-for-less-in-notepad/
"How to enable syntax highlighting for LESS in Notepad++"). However, ended up not
using LESS because I don't need all its functionalities.  Right now my styling 
is pretty simple; the only thing I'd probably want to use is the scoped styling,
but including LESS just for that seems overkill.

While styling the blog categories/tags/comments I also came across this
useful page about CSS shorthands: [CSS Shorthand 
Guide](http://www.dustindiaz.com/css-shorthand/ "CSS Shorthand Guide").

05.16.2012
----------

While structuring the big layout, I decided to play around with the new HTML5
form features.  I found this page really useful to decide which features to use
based on browser support: [The Current State of HTML5 
Forms](http://wufoo.com/html5/ "The Current State of HTML5 Forms").

I also found [HTML5Pattern](http://html5pattern.com/ "HTML5Pattern"), which 
lists common patterns to use in the new form elements.  I have no use for it 
myself right now, but it looks like it'd be really handy for anyone that would 
need patterns!

05.18.2012
----------

As I've been working on this, I've been checking how it looks in Chrome 18,
Safari 5, Firefox 12, Opera 11, and Internet Explorer 9.  I decided to try out
the new HTML5 "search" input type.  It's pretty neat; in Chrome and Safari,
whenever there is text in the box, an "x" appears that you can click to clear
the text.

I also decided to try out the "placeholder" attribute in forms, and it seems 
that they all support it except IE (surprise surprise).  However, I noticed 
something interesting - when I use "text-align: center" in the input box, 
Chrome, Firefox, and Opera center the placeholder text, but Safari leaves it 
left-aligned, while centering text that's typed in!

In searching for a way to center Safari's placeholder text, I came across [HTML5
Placeholder Styling with CSS](http://davidwalsh.name/html5-placeholder-css 
"HTML5 Placeholder Styling with CSS").  I was able to change the color of 
Safari's placeholder text with the "::-webkit-input-placeholder" selector, but 
unfortunately using "text-align: center" there did not center the placeholder 
text either.  I guess I'll just have to leave it that way.

05.20.2012
----------

I've decided not to center the text in my search box.  I also realized that I
should add some sort of search button, instead of assuming the user will always
just press "enter" to search.

Now I've discovered a problem where even when I give both the search input and
the button explicit heights that are the same, some browsers make them different
heights, while others make them the same height but they are vertically
aligned differently - none of them show it the way I expect!

I found this article about [Equal height inputs and 
buttons](http://christophzillgens.com/en/articles/equal-height-input-and-button-elements-in-firefox-and-safari
"Equal height inputs and buttons"), but it didn't seem to be the exact same
problem.  I also didn't want to use a vendor-prefix as a fix.

It turns out that if I use an input of type "button" instead of a button 
element, the problem is gone!  I wonder why?

Also, I am starting to add CSS3 styling, and [CSS3 Please](http://css3please.com/
"CSS3 Please") is awesome.  It's so useful to have all the vendor prefixes
gathered in one place... plus it's so handy that all the values in the different
prefixes change when you edit just one of them!

05.22.2012
----------

Decided to change the search bar style again, so that the search input box and
the submit button are within a surrounding box.  However, "background-color: 
transparent" doesn't work on input boxes in Chrome or Safari!  Why???

I found this Stack Overflow question: [HTML5 Search Input: No Background Image
in Chrome?](http://stackoverflow.com/questions/2992215/html5-search-input-no-background-image-in-chrome
"HTML5 Search Input: No Background Image in Chrome?") It turns out that WebKit
supports the "search" input type (hence the "x" to clear the box), but it has
its own styling for it that is not accessible yet.  The other browsers don't
seem to support the "search" input type, so it styles them normally as "text"
input types.

The solution in the answers is to use "-webkit-appearance: none".  Works for me!

Also found [WebKit HTML5 Search 
Inputs](http://css-tricks.com/webkit-html5-search-inputs/ "WebKit HTML5 Search
Inputs"), which seems like it might be helpful later on.