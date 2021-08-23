# **CSS Notes**
---
## *Definitions w/Examples*
---
#### In order to select specific items you must use the tag from html to identify what CSS will do
###### *CSS*
```CSS
h1 {
  color: red
}
```
##### This is called a CSS Block ^
###### *HTML*
```html
<h1>This Is My Header</h1> 
```
#### This will change anything in the tag called out to be red
---
In order to select multiple tags for different CSS just make a new block and seperate similar tags the `id=` attribute or `class=` attribute
```html 
<p id="id tag here"></p>
<span class="class tag here"></span>
```

```CSS
h1 {
  color: red;
}
 
p {
  font-weight: bold;
}

#id {
    font-size: 15pt
}

.class {
  font-weight: bold;
}
```
---
---
### *CSS Selectors*

* #### Compound
```CSS
h1, h2, #box {
  font-family: Arial, Helvetica, sans-serif;
}
```
^This selects all matched elements in the compound set. This selector is indicated by a `,` comma separating the selectors of the set. Each element within the comma separated list will be styled the same.

* #### Descendent
```CSS
#nav li {
  background: blue;
}
```
^This selects an element that is nested inside of the specified parent element. This selector is indicated by a keyboard space between the parent and the child to be selected.

* #### Child
```CSS
#list > li {
  border: 1px solid black;
}
```
^This selects an element that is nested only one level deep inside of the specified parent element. It only selects direct children and not grandchildren. This selector is indicated by a `>` (greater than) symbol between the parent and the child to be selected.

* #### Adjacent Sibling
```CSS
h3 + p {
  color: green;
}
```
^This selects an element that appears directly after the former element assuming they are both siblings (in the same level of nesting, in the same parent). This selector is indicated by a `+` plus symbol between the former sibling and the selected element that follows.

* #### General Sibling
```CSS
h2 ~ p {
  color: black;
}
```
^This selects all elements that appear directly after the former element. This selector is indicated by a `~` tilde symbol between the former sibling and the selected element that follows it

* #### Universal
```CSS
* {
  color: orange;
}
```
^This selects elements where the properties specified have not been styled by any other selectors. This selector is indicated by an `*` asterisk symbol.

* #### Attribute
```CSS
img[alt="Cat"] {
  border: 1px solid black;
}
```
^This selects an element with a matching attribute value. This selector is indicated by `[]` square brackets, followed by the attribute property and value of the selected element within the brackets.

---
---
* #### Other Attribute Selectors:
```CSS
a[href^="http"] 
```
^The `^=` caret symbol and equals sign select elements that start with the matching value, such as `<a href="http://google.com">google</a>`

---
```CSS
p[class$="dog"] 
```
^The `$=` dollar and equals signs select elements that end with the matching value, such as `<p class="bigbdog">...</a>`

---
```CSS
img[alt*="love"]
```
^The `*=` asterisk and equals sign select elements that have the matched characters appearing anywhere within the value, such as `<img src="myimage.jpg" alt="I love you.">`

---
```CSS
p[class~="monkey"] 
```
^The `~=` tilde symbol and equals sign select elements that contain the term within a space separated value, such as `<p class="zoo monkey details">...</p>`

---
```CSS
p[class|="birds"] 
```
^The `|=` pipe symbol selects elements that contain the term within a dash separated value, such as `<p class="new-birds-today">...</p>`

---
#### Psuedo Class
```CSS
a:link {
  text-decoration: none;
}
```
^This selects an element based on the unique relationship or state described in the selector. This selector is indicated by the `:` colon symbol, followed by the pseudo class that describes the element's state or positioning amongst other elements.

* #### Other Psuedo Selectors:
```CSS
a:link
```
^selects links in their default state before the visitor has interacted with them.

---
```CSS
a:visited 
```
^selects links after the user has already clicked on them and is visiting that page again.

---
```CSS
a:hover
```
^selects links when the user is hovering their mouse over the link.

---
```CSS
a:active 
```
^selects links for only the moment when the mouse button is pressed when clicking on the link.

---
```CSS
p:first-child
```
^selects elements that are the first child when appearing inside a common parent. Such as:
###### *HTML*
```html
<div><p>I'm selected</p><p>I'm not</p><p>Neither am I</p></div>
```
---
```CSS
p:last-child
```
^selects elements that are the last child when appearing inside a common parent. Such as:
###### *HTML*
```html
<div><p>I'm not selected</p><p>Neither am I</p><p>I'm selected</p></div>
```

---
See video on CSS "Styling the Front-End": https://youtu.be/-k-1TU8qq0Q?t=9
