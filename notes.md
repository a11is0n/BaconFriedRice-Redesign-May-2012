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