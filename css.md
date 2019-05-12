- tutorial...  
<https://www.youtube.com/watch?v=UB1O30fR-EE&t=154s>

- can include css file externally or put a STYLE tag inside the HEAD area
- can also use inline css attributes, but just don't.
- style type="text/css" (type is not required, but good practice)

- .class-name {} or #id-name {}

- css lines end with ';'

---

- tutorial...  
<https://www.youtube.com/watch?v=yfoY53QXEnI>

- css can be done in many different ways
- flexbox = css3 layout mode

- can be extended with Sass/Less (to add functionality)

- convention: keep structure, style, functionality as seperate as possible

- 3 ways of adding css:
1. INLINE CSS (similar to a tag attribute (style="css code") - don't do this)
2. INTERNAL CSS (using \<style> type="text/css" tags in head of html doc) - this css can only be used in 1 file though
3. EXTERNAL CSS (BEST - link an external css stylesheet, link to css file)

- can grab onto elements (either individually, chunks or dispersed with id/class or tag name directly)
- e.g. h1{css code}
- note: the thing before the {} is called the SELECTOR
- note: selectors have accumulative "SPECIFICITY" depending on the tag < class < id combo applies to them.

- syntax: selector { property:value; }
- ';' is needed as a declaration seperator

- color property (color contained text)
- background-color (color background of element)

- I believe that the most specific style declaration is used (e.g. color in body #main-header overrides color given to it by body)

- colors (name, html5name, hex(3/6), rgb/a)

- ALTERNATES: e.g. font-family: Arial, Helvetica, sans-serif; means that if Arial can't load then use Helvetica

- web-safe fonts work without need to import fonts as stylesheets
- Times New Roman is default w/ 16px

- can use font: property to combine all other properties (similar cases with other properties as well)

- UNITS: px, em (responsive unit, relative to font size of the element)

- name stuff like: box-1 rather than box1

- ID (unique), CLASS (reusable)
- sometimes CLASS-ONLY (see bootstrap framework)

- shortcut: #333333 can be truncated as #333

- tip: use margin:0 to remove the inherent margin to a block (does not affect headings since they have their own margin within wrapper element)

- margin:auto (auto-space around an element), can wrap a container div around elements and then set the container width/height to a fixed size

- tip: use percentages for sizes in order to make element sizes responsive to different screens/windows

- there exists a BOX MODEL (content < padding < border < margin)

- shorter syntax: margin: TOP RIGHT BOTTOM LEFT or TOP/BOTTOM LEFT/RIGHT or ALL

- tip: *{} is a wildcard that means for every element apply this style (within declaration). Known as a "RESET", you could use it to set margin:0; padding:0; and then go from there...

- note: no need to specify a unit when working with 0.

- COMBINED SYNTAX: e.g. .box-1 h1 {} would style every h1 header within box-1 class.

- LINK STATES:  
a:hover {}  
a:active {}  
a:visited {}

- **NOTE**: within a style declaration, if you have 2 lines that affect the same sort of thing (e.g. color:red; color:green; then the lower line will take effect). But if you had something like padding:1px; and then padding-left:20px then maybe it applies the 20px left and 1px elsewhere? 

- tip: can use url(..) to import and image to display with a style (e.g. custom bullet point)

- bootstrap uses form-group for the div class

- tip: try to fully qualify names whenever possible

- note: can do something like input[type="text"] {} to style only text input

- tip: if we want to apply the same style code to multiple elements, we can do something like .class1, .class2 {}

- ALIGNMENT:  
have a div containing a bunch of elements called say "block", then apply .block{float:left; width:100%/numberofelements}. this aligns the child elements horizontally.
- note: if we do this and then adding padding, it will overflow the sizes and push some child elements onto new line. To prevent this from happening, add a box-sizing:border-box; (this makes it take into account the padding,border,etc. into the width calculation)

- tip: use flexbox to work with alignment better.

- **note**: when you float stuff, the next markup with get screwed up, so you need to clear it. use div class="clr" below previous div and then use .clr {clear:both;} put this div after any elements that get floated?

- tip: you could write your css file top to bottom from most global style to most local. But, file order only matters when same property matches multiple selectors of same specificity.

- POSITIONING:  
static (default, render elements in order of document flow)  
relative (relative to natural pos)  
absolute (target pos within relative  parent element)  
fixed (fixed within browser window)  
initial (sets property to default value)  
inherit (inherit property of parent element)

- e.g. set position:relative in parent element and then position:absolute; top:100px in the child element puts its 100px down within parent element

- this type of positioning is useful for browser games

- position:fixed keeps elements at same position on screen no matter scrolling (good for navbars)

- use background-image:url(".."); to paste an image as background of an element

- PSEUDO-CLASSES  
e.g. .my-list li:first-child {} (only selects the first list element to apply style to)  
note: INDEXED FROM 1, if we want the n-th element then use nth-child(n){}  
can also do nth-child(even/odd){}

- use overflow:hidden to prevent scrollbars from showing up even if content goes outside its bounds

- tip: use MEDIA QUERIES to make elements more responsive



---


 