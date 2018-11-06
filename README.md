# Emmet

Boostrap site showcasing samples of using Emmet to quickly generate HTML templates and snippets.

Built using npm for resource management - Bootstrap, jQuery, Underscore.js and coded using Brackets.

**Tools Required:**

- **<a href="http://brackets.io/" target="_blank">Brackets</a>**
- **<a href="http://emmet.io/" target="_blank">Emmet</a>**

**Additional Dependencies**

- **<a href="http://getbootstrap.com/" target="_blank">Bootstrap</a>**
- **<a href="http://jquery.com/" target="_blank">jQuery</a>**
- **<a href="https://nodejs.org/en/" target="_blank">Node.js</a>**

## Basic Example:

For starters, this is all that was required to create the beginning HTML5 structure for this page.

	html:5

Typing this into Brackets and hitting the tab key, results in the following HTML5 template being rendered:


	<!DOCTYPE html>
		<html lang="en">
		<head>
    		<meta charset="UTF-8">
    		<title>Document</title>
		</head>
		<body>
    
		</body>
	</html>

## Generate lorem ipsum

Generate a div with 5 paragraphs, each with 100 words of lorem ipsum.

	div>(p>lorem100)*5

Generate an un-ordered list with 5 list items, each with 10 words of lorem ipsum.

	ul>(li>lorem10)*5


## A More Elaborate Example:

There are a quick Emmet shortcuts for generating HTML for headers, divs, paragraphs, lists, tables, etc. But, the real power comes from stringing several of the shortcuts together. For example, the following might be the requirements for a chunk of HTML that needs to be quickly spun up for a real project or just for tinkering.

The requirements are:

- A div with an id of 'container'
- With a h1 with a class of 'header1'
- With a sibling h2 with a class of 'header2'
- With a sibling p with 10 words of lorem ipsum
- With an unordered list
- Containing five list items, each with a hyperlink
- And another p of 10 words of lorem ipsum at the level of the first p

This would be coded in Emmet like this:

	div#container>h1.header1+h2.header2+p>lorem10^ul>li*5>a^^p>lorem10 [tab key]

Result:
  
	<div id="container">
		<h1 class="header1"></h1>
		<h2 class="header2"></h2>
		<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Similique, in!</p>
		<ul>
			<li><a href=""></a></li>
			<li><a href=""></a></li>
			<li><a href=""></a></li>
			<li><a href=""></a></li>
			<li><a href=""></a></li>
		</ul>
		<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Incidunt, dolores.</p>
	</div>

**Another example using Groups**

In this example, the parenthesis are wrapped around groups of expressions to keep them at the same level.

	div.wrapper>div.header(h1+h2+p)+(ul>li*3)+div.footer

Result:

	<div class="wrapper">
		<div class="header">
			<h1></h1>
			<h2></h2>
			<p></p>
		</div>
		<ul>
			<li></li>
			<li></li>
			<li></li>
		</ul>
		<div class="footer"></div>
	</div>