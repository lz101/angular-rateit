# angular-rateit

This directive was inspired by the jQuery (star)rating plugin [RateIt](http://rateit.codeplex.com/).
However this package will work without jQuery and is super light weight: 3.3 Kb minified 1.9 Kb.

## Getting Started

You can install an angular-rateit package very easily using Bower:

```shell
bower install angular-rateit
```

Or add the files manually to your index file:

```html
<link rel="stylesheet" href="angular-rateit/dist/rateit.css" />
<script src="angular-rateit/dist/rateit.js"></script>
```

Finally add 'ngRateIt' to your main module's list of dependencies:

```js
angular.module('myApp', [
	...
    'ngRateIt',
    ...
]);
```

## How to use

To get it working simply add this block of code to your view:

```html
<ng-rate-it ng-model="test.rateit"></ng-rate-it>
```

For more advanced functionality you can add a couple attributes:

```html
<ng-rate-it 
	ng-model = "String, Number, Array"
	min = "Double"
	max = "Double"
	step = "Double"
	readonly = "Boolean"
	ispreset = "Boolean"
	resetable = "Boolean"
	starwidth = "Integer"
	starheight = "Integer"
	rated = "Function"
	reset = "Function"
	over = "Function"
	beforerated = "Function: return promise"
	beforereset = "Function: return promise"
	>
</ng-rate-it>
```

### Attributes

| Attribute | Description | Value | Default |
|---|---|---|---|
| ng-model    | Object bound to control. (Required) | String, Number, Array | - |
| min         | Minimal value. | Double | 0 |
| max         | Maximal value. The difference between min and max will provide the number of stars. | Double | 5 |
| step        | Step size. | Double | 0.5 |
| readonly    | Whether or not is readonly. | Boolean | false |
| ispreset    | Whether or not the current value is the initial value. | Boolean | true |
| resetable   | When not readonly, whether to show the reset button. | Boolean | true |
| starwidth   | Width of the star picture. | Integer | 16 |
| starheight  | Height of the star picture.  | Integer | 16 |
| rated       | Fired when a rating happened. (Obtain the rated value by the model) | Function | - |
| reset       | Fired when the reset button was clicked. | Function | - |
| over        | Fired when hovering over the element. First function parameter is the event, second parameter will contain the hover rating value. | Function | - |
| beforerated | Fired before the item is actually rated. By rejecting the promise it is possible to cancel the rating. | Function: return promise | - |
| beforereset | Fired before the item is actually reset. By rejecting the promise it is possible to cancel the reset. | Function: return promise | - |
