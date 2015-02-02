# Angular Mmultiple Selection Module
Simplest way to make your angular items selectable

[Simple Demo](http://maxazan.com/angular-multiple-selection/)

[Image selection Demo](http://maxazan.com/angular-multiple-selection/)

##Installation

###Using npm
```
npm install angular-multiple-selection
```

###Using bower
```
bower install angular-multiple-selection
```

###From source

Download [source](https://github.com/maxazan/angular-multiple-selection/archive/master.zip) from github.com

##Using
* Add `multiple-selection.min.js` file to your application
```html
<script type="text/javascript" src="multiple-selection.min.js"></script>
```
* Add module to your app `angular.module('app', ['multipleSelection'])`
* Add `multiple-selection-zone` attribute to element where selectable items will be located
* Add `multiple-selection-item` attribute to each selectable item
* Customize css


##How it works
Each selectable item has it`s own angular scope with variables

| Name  | Description |
| ------------- | ------------- |
| isSelectable  | `true` if element can be selected |
| isSelecting  | `true` if element now selecting. It means it enters in selection rectangle when you dragging |
| isSelected  | `true` if element selected |

###How to customize

* Add `ng-class` to your item
```html
<div multiple-selection-item ng-class="{'selecting': isSelecting ,'selected': isSelected}"></div>
```
* Customizing `.selecting` and `.selected` in your css
```css
.selected {
    background-color: green !important;
}
.selecting {
    background-color: yellow !important;
}
```
* You can also customize your rectangle for selecting
```css
.select-helper {
      position: absolute;
      border: 1px dashed red;
      background: red;
      opacity: 0.2;
}
```
