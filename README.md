# Code-Refactor

## This is an on-the-job ticket assignment to clean up the given code

## User Story

```
AS A marketing agency
I WANT a codebase that follows accessibility standards
SO THAT our own site is optimized for search engines
```

## Acceptance Criteria

```
GIVEN a webpage meets accessibility standards
WHEN I view the source code
THEN I find semantic HTML elements
WHEN I view the structure of the HTML elements
THEN I find that the elements follow a logical structure independent of styling and positioning
WHEN I view the icon and image elements
THEN I find accessible alt attributes
WHEN I view the heading attributes
THEN they fall in sequential order
WHEN I view the title element
THEN I find a concise, descriptive title
```
## My Implementation

I began by looking through the `index.html` and noticed that the elements were not cascaded in a way that was easily read. For example

From this...
```html
<nav>
<ul>
<li>
<a href="#search-engine-optimization">Search Engine Optimization</a>
</li>
</ul>
</nav>
```
To this...
```html
<nav>
    <ul>
        <li>
            <a href="#search-engine-optimization">Search Engine Optimization</a>
        </li>
    </ul>
</nav>
```
While doing this I also noticed that there were no semantic html elements defining parts on the page, so I removed and added them where necessary. For example

From this...

```html
<div class="content">        
    <div id="search-engine-optimization" class="search-engine-optimization">
</div>
```
To this...
```html
<section class="content">
    <div id="search-engine-optimization" class="search-engine-optimization">
</section>
```

I then added the `alt` attribute to all the `<img>` tags so that I can name them based on what is being displayed. For example

```html
<img src="./assets/images/search-engine-optimization.jpg" class="float-left" alt="Desk with booklet that says SEO" />
```
This allows the image to be better accesible because it has a description.

I then began looking at the `style.css` file and noticed that a lot of the css rule sets were redundant. Some of them were created sperate however contained the exact same declarations. To simplify this I combined the class selectors into one rule set based on what was the same. For example 

```css
.benefit-lead, .benefit-brand, .benefit-cost
{
    margin-bottom: 32px;
    color: #ffffff;
}
```
The commas specify each new class selector that will use the declarations specified.

You can view the working site here [Code Refactor](https://nkrilis.github.io/Code-Refactor/)
Thank you :smiley:

![Code Refactor](./assets/images/01-html-css-git-homework-demo.png)
