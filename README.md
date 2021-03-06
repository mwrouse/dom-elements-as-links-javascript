# DOM Elements as Links
This little JavaScript library allows you to have any element on a page act as a link, even if it is not an anchor tag.

## Syntax
The syntax for using any DOM Element as a link is extremely simple, all you do is add an href attribute to the element, and an option target attribute, just like you do on &lt;a&gt; tags.
```html
<span href="http://example.com">This is a link!</span>
<span href="http://example.com" target="_blank">This is a link that opens in a new tab!</span>
<img src="http://example.com/user/profile/avatar.png" href="http://example.com/user/profile">
```

## Styling
If you're interested in styling your non-anchor tag links the same way as your anchor tag links, this is also simple, add CSS similar to the following:
```css
a,
[href]
{
  /* CSS Styling Here */
}
a:hover,
[href]:hover
{
  /* Styling for Hover */
}
```
Yes, this is a bit redundant, seeing as all you need is the [href] selector, but oh well.

Please, however, at least have this CSS somewhere:
```css
[href]:not(a)
{
  cursor: pointer;
}
```
## Usage
To use this library, simply include the source code in your program, or copy and paste it into an existing JavaScript file you have, then run
```javascript
window.DOMElementsAsLinks()
```
when the page is done loading. It is important that it is ran when the page has finished loading, because all DOM elements need to be ready for it to read them.

You can do this by one of the following ways:
```javascript
window.onload = function(){
  window.DOMElementsAsLinks();
};

```
```javascript
window.addEventListener('load', function(){
  window.DOMElementsAsLinks();
});
```
You should know how to do that though.

## Example
[View a CodePen Example](http://codepen.io/mwrouse/full/aNZxJJ/)

## Known Issues 
The only known issue is that this won't work on browsers that have JavaScript disabled...

## License
Distributed under the [MIT license](https://raw.githubusercontent.com/mwrouse/dom-elements-as-links-javascript/master/LICENSE).
