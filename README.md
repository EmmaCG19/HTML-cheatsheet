# HTML-cheatsheet 

<img src="https://icreate.agency/wp-content/uploads/2015/10/html5-1300x470.gif" alt="drawing" height="300" width="100%"/>

## Structure

```html
<!DOCTYPE html>
<html>
<head>
  <title>My webpage</title>
</head>
<body>
  <div>
    <h1>Main title</h1>
  </div>
</body> 
</html>

<!--Make a comment--> 
```

## Head
### Metadata

`<meta lang = "en-US">` Defines language

`<meta charset="utf-8">` Defines charset

`<meta name="keywords" content="HTML, CSS, javascript, XML">` Defines keywords used by searchengines

`<meta name="description" content="my description">` Defines description of the webpage

`<meta name="author" content="John Doe">` Defines author of the website

`<meta http-equiv="refresh" content="30">` Defines refresh-span of webpage

`<meta name="viewport" content="widt=device-width, initial-scale=1.0">` Defines webpage viewport

### Title

`<title> Website </title>`

### Add external files

`<link rel="stylesheet" type="text/css" href="stylesheet.css">` Link a stylesheet

`<script src="javascript.js" type="text/javascript"></script>` Link a script

## Body
### Text

<!-- Esto es un comentario -->

`<p id="" style="" class="" title="tooltip">` Paragraph

`<b>` Bold text

`<strong>` Important text _(recommendable)_

`<i>` Italic text 

`<em>` Emphasized text _(recommendable)_

`<mark>` Marked text

`<small>` Smaller text

`<del>` Deleted text

`<ins>` Inserted text

`<sub>` Subscript text

`<sup>` Superscript text

`<q>` Short quotation

`<blockquote cite="url">` Quotation from another site

`<abbr title="Fullname">` Abbreviation or acronym text

`<address>` Defines contact information of a document or article

`<cite>` Defines the title of a work

`<bdo dir="rtl | ltr">` Bi-directional override _[right-to-left | left-to-right]_

`<mark>` Marked text

`<time datetime="2008-02-14 20:00">` Add time/datetime 

`<code>` Defines a code section with _monospace font_

`<kbd>` Defines a keyboard input

`<samp>` Defines an output 

`<pre>` Preserve white spaces in the code section

`<var>` Defines a variable 	

### Line-break

`<br>` Breakline

`<hr>` Horizontal Rule

__(*)__ *Don't require a closing tag*

### Heading

`<h1>` Heading used for a main title. _It's a good practice to have only one._

`<h2>` Heading used for section titles.

`<h3>`

`<h4>`

`<h5>`

`<h6>` This is the smallest heading

### Container

`<div>` Block-level element

`<span>` Inline-level element 

### Hyperlink

`<a href="external_url|/rootFolder/file.ext|sameFolder.ext" target="_blank|_self|_parent|_top">`

### Bookmark

`<p id="C4"></p>` Add a bookmark

`<h1 id="anotherpage.html#C4">Go to</h1>` Navigate to a bookmark

### Images
#### Add an image

`<img src="url|localpath" alt="Alternative text" width="100" height="100"/>` 

#### Add an image with clickable areas

```html 
<img src="example.jpg" alt="An_example" usemap="#exampleMap" width="100" height="100">

<map name="exampleMap">
  <area shape="square" coords="34,44,270,350" alt="shape1" href="https://...">
  <area shape="rect" coords="290,172,333,250" alt="shape2" href="https://...">
  <area shape="circle" coords="337,300,44" alt="shape3" href="https://...">
</map>
```

#### Set different images depending of the viewport size

```html
<picture>
	<source media="(min-width: 650px)" srcset="image1.png"> 
	<source media="(min-width: 465px)" srcset="image2.png">
	<img src="image3.jpg">
</picture>
```

### List
#### Unordered list

```html
<ul style="list-style-type:circle|square|disc|none;">
	<li>Unordered list item</li>
	<li>Unordered list item</li>
	<ul style="list-style-type:circle|square|disc|none;">
	  <li>Unordered list item inside another unordered list</li>
		<li>Unordered list item inside another unordered list</li>
	</ul>
</ul> 
```

#### Ordered list

```html
<ol type="1|A|a|I|i">
	<li>Ordered list item</li>
</ol>
```

#### Description list

```html
<dl>
  <dt>Item</dt>
  <dd>Item description</dd>
</dl>
```

### Table

```html
<table>
  <caption>Example</caption>
<thead>
  <tr>
    <th>Header-1</th>
    <th>Header-2</th>
    <th>Header-3</th>
  </tr>
</thead>
<tbody> <!--Body-->
  <tr rowspan="1"> <!--Row-->	
    <td colspan="2">Col-1</td>
    <td>Col-2</td> 
  </tr>
</tbody>
<tfoot> <!--Footer-->
  <tr>
    <td>Footer</td>
  </tr>
</tfoot>
</table>
```

### Frame

`<iframe src="/pages/page.html" name="iframe_a"></iframe>` Show another page inside the frame

`<a href="url" target="iframe_a">` Load the linked website inside the targeted frame

### Files location:

`<img src="file.png">` Same folder

`<img src="images/file.png">` Subfolder of the current folder

`<img src="/images/file.png">` Subfolder of the root folder

`<img src="../file.png">` Inside the root folder

### Content model (SEO)

Tag | Description
--- | -------------
`<header>` | Defines a header for document or section
`<nav>` | Defines a container for navigation links  
`<section>` | Defines a section in a document 
`<article>` | Defines a independent self-contained article (forum post, blog post, newspaper article) 
`<aside>` | Defines a Sidebar
`<footer>` | Defines a footer for a document or section (copyright, author, address, external links)
`<detais>` | Defines additional details
`<summary>` | Defines a heading for `<details>`
`<figure>` | Groups a caption and its explanation  

#### Example

```html
<figure>
	<img src="" alt=""/>
	<figcaption>This is an explanation</figcaption>
</figure>
```

## Form 
### Example

```html
<form action="#" method="get" target="_self" novalidate=""> 
  <input type="number" name="" id="" class="" value= "33"/>
  <input type="text" name="" id="" class="" value="John Doe"/>
  <input type="submit" id="" class="" value="Submit"/> 
</form>
```

### Attributes

`method="get|post"`: http method 

#### GET
- Appends form-data into the URL in name/value pairs
- The length of a URL is limited (2048 characters)
- Never use GET to send sensitive data! (will be visible in the URL)
- Useful for form submissions where a user wants to bookmark the result
- GET is better for non-secure data, like query strings in Google

#### POST
- POST has no size limitations, and can be used to send large amounts of data
- Form submissions with POST cannot be bookmarked

`action="/page.php|#"`: form destination page 

`target="_self|_blank"`: submit response location

### Input

`<input type="tel" placeholder="123-45-678" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}" title="National number" readonly>` Phone number

`<input type="text" maxlength=50 size="30">` Text with characters limit

`<input type="password" autofocus>` Password with autofocus

`<input type="email" pattern="regEx" required>` Email with regex validator

`<input type="url" name="url" id="url" placeholder="https://example.com" pattern="https://.*" size="30">` Url

`<input type="color">` Color picker

`<input type="date" min="englishFormat" max="englishFormat">` Date picker

`<input type="datetime-local">` Datetime picker

`<input type="time">` Time picker

`<input type="week">` Week picker

`<input type="month">` Month picker

`<input type="number" min="minValue" max="maxValue" step="intervalValue">` Counter

`<input type="range" value="maxValue">` Range picker 

`<input type="file" name="files" multiple>` Accept more than one value for the input

`<input type="hidden" id="custId" name="custId" value="3487">` Hide input information from the users

`<input type="button" disabled>` Basic Button 

`<input type="submit">` Submit button

`<input type="reset">` Reset button

`<input type="image" src="example_submit.gif" alt="Submit">` Submit button with an image

`<input type="search" autocomplete="on">` Search box

### Textarea

```html
<textarea name="fmensaje" rows="10" cols="30">
	Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
	tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
	quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
	consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
	cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
	proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
</textarea>
```

##### Checkbox

```html
<label for="prueba1">Prueba 1</label>
<input type="checkbox" id="prueba1" value="prueba1">
<label for="prueba2">Prueba 2</label>
<input type="checkbox" id="prueba2" value="prueba2" checked> 
<label for="prueba3">Prueba 3</label>
<input type="checkbox" id="prueba3" value="prueba3"> 
```

##### Radiobutton

```html
<label for="prueba1">Prueba 1</label>
<input type="radio" id="prueba1" checked> 
<label for="prueba2">Prueba 2</label>
<input type="radio" id="prueba2"> 
<label for="prueba3">Prueba 3</label>
<input type="radio" id="prueba3" name="prueba3" value="prueba3"> 
```

#### Fieldset

```html
<fieldset>
	<legend>Detalle de la seccion</legend>
	<label for=""></label>
	<input type=""/>
	<label for=""></label>
	<input type=""/>
	<label for="inputElement"></label>
	<input type=""/>
</fieldset>
```

#### Dropdown-list

Defines an input element with a list of predefined-options where one must be selected

```html
<select name="values" size="3" multiple>
	<option value="1">Algo</option>
	<option value="2">Algo</option>
	<option value="3">Algo</option>
	<option value="4" selected>Algo</option>
</select>
```

#### Data-list

Defines an input element with a list of predefined-options that act like suggestions

```html
<input list="browsers">
<datalist id="browsers" name="fbrowser"> 
	<option value="Internet Explorer">
	<option value="Chrome">
	<option value="Opera">
	<option value="Vivaldi">
</datalist>
```

#### Button

`<button type="button|submit" onclick="clickOnMe()" disabled>My button</button>`

## Extra
### Tips

1. Validate your code with W3C markup validation.
2. Identation is crucial
3. Avoid Excessive comments
4. Use lowercase

## Sources

[W3Schools](http://w3schools.com)

[W3C content model](https://www.w3.org/TR/2011/WD-html5-20110525/sections.html)
