- cheatsheet...  
<https://web.stanford.edu/group/csp/cs21/htmlcheatsheet.pdf>

- naming conventions...  
<https://www.lifewire.com/naming-html-files-3466503>

- tutorial...  
<https://www.youtube.com/watch?v=UB1O30fR-EE&t=154s>

- can write text outside any elements and it will render

- ELEMENT (either OPENING TAG + CLOSING TAG or SELF-CLOSING TAG)

- convention: use " />" for self-closing tags to be consistent and for backwards-compat

- HEAD (meta-info, some used by google)
- BODY (display stuff)

- DOCTYPE (HTML4? HTML5? XHTML?, etc.)

- INLINE ELEMENTS (do not start on newline + take only necessary width)
- BLOCK ELEMENTS (start on newline + take full width available)

- STRONG TAG replaces BOLD tag
- EM TAG replaces italic tag

- tip: add a target="_blank" attribute to a link in order for it to open the link in a new tab

- a link can be relative or absolute (e.g. use https://...)

- TAG ATTRIBUTES (key-value pairs), all tags can have attributes (provide info about element)

- NAVBARS are usually just styled unordered lists

- historically, tables were used for webpage layout (but now we have css!)

- FORM (just structure, no functionality)  
action="\<phppage>"  
method="POST" (make post request to server), like add data to a database
method="GET" (fills in data in the URL, UNSAFE)

- INPUT  
type="" (different input types, usually use "text"), "email" type has some built in validation, "date" (calendar selector), "submit" (makes button)  
name="" (identifier from database for example)  
value="" (default value that gets displayed)
placeholder="" (similar to value except the text is greyed out and dissapears on click), had to use JS before

- usually use css rather than \<br /> for spacing

- BUTTON  
click="someFunction" (event to use in JS)

- IMG (inline)  
src="../\<path from parent dir>"  
alt="" (if image cant be found/renderer, display some backup text)
width/height="" (preserves aspect ratio if you only set one, since other is set to "auto")

- can wrap an image in a link (so that when you click on image it can go somewhere, or even open up image in fullscreen)

- BLOCKQUOTE  
cite="" (where the quote comes from)

- ABBR  
title="" (the abbreviation expanded)

- CITE (italic style)

- HTML5 SEMANTIC TAGS (describes its meaning to the developer and to the browser)
- each defines an area on the page...
- header (logo, social media links)
- nav (navbar)
- section (copy text)
- article (around each post of a blog)
- aside (sidebar content)
- footer (copyright, policy, etc.)
- main
- details

- note: these are purely for semantic reasons, the structure doesn't change (ex. could put footer at top of page if we wanted to). can also have multiple of each element if you so choose (ex. each blog post title could be wrapped inside its own header)

- note: any? element after a block element will be pushed onto a new line

- tip: use href="#" to link to current page

- use nav tag to wrap something related to navigation

- convention: id/class strings should be lower-case-hyphenated

- META TAGS (for search engine inspection)  
name="" (type), such as description, keywords, etc.  
content="" (actual content)
