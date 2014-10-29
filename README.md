Coat.js
=======

Coat.js is a JQuery plugin for point based reveal for HTML elements. 


Features
--------

- Light weight
- Selective CSS
- Multiple rules
- Easy to use
- Easy to understand


Usage
-----


1. Ensure to include the latest JQuery version
2. Download the `coat.js` file and reference the it from your HTML.

```html
<script src="//ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>
<script src="lib/coat.js"></script>
```


To apply `coat.js` to your elements, in your JavaScript, use:
```javascript
$("#selector").coat();
```

Examples
--------

If you'd like to have coat.js affect multiple elements, you can use either classes or a selector that gives multiple elements.
```javascript
$(".selector1, selector2, p").coat();
```

`coat.js` also accepts some special rules
```javascript
$("#seletor").coat({
	css: {
		"color": "white"
	},
	pointSelector: ".changepoint"
});
```

Rules
-----

Currently, there are 3 rules that you can apply to an element with `coat.js` enabled

#### `pointSelector`
The default selector that `coat.js` uses is `.coat`. You can customize this by adding the `pointSelector` attribute to your newly initialized coat element. This can be done with:
```javascript
$("#element").coat({
	pointSelector: ".betterCoat"
});
```
This changes the element that the element is revealed on to the class `betterCoat`.
**Note:** by applying the `pointSelector` attribute, you ignore the defualt coat selector (`.coat`).

#### `css`
The `css` attribute allows you to apply the specified CSS rules to the second element that is created.

An example of this is when you you scroll past your point, you want the color of the text in your coat element to change to green. That can be done simply with:
```javascript
$("#element").coat({
	css: {
		"color": "green"
	}
});
```
**Note:** By default, `coat.js` changes the CSS `color` attribute to red. This is only for testing purposes. You are encouraged not to make anything on your webpage hard red.
