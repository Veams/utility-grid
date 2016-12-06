<p align="right">
    <a href="https://badge.fury.io/bo/veams-utility-grid"><img src="https://badge.fury.io/bo/veams-utility-grid.svg" alt="Bower version" height="20"></a>
    <a href="https://gitter.im/Sebastian-Fitzner/Veams?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge"><img src="https://badges.gitter.im/Sebastian-Fitzner/Veams.svg" alt="Gitter Chat" /></a>
</p>

# Grid

Bourbon Neat provides a simple grid system, which you can use in your projects. 

With `u-grid` there is implemented a mobile first class based system which is like Bootstrap or Foundation, but you are also flexible enough to just use mixins in your Sass or SCSS files. 

In general `u-grid.scss` generates a set of grid column classes using namespaces.

------------

## Requirements
- Bourbon Neat in Beta => _http://neat.bourbon.io/ => `bower i neat#v2.0.0.beta.1 --save-dev`_
- wrapWith helper => _https://www.npmjs.com/package/mangony-hbs-helper-wrap-with => `npm i mangony-hbs-helper-wrap-with --save-dev`_

### Documentation
- Bourbon Neat: _http://thoughtbot.github.io/neat-docs/2-0-0-beta-1/ _

------------

## SASS

### Variables 

- $grid-defaults {`Object`} [`(columns: 12, gutter: 52px)`] - _Default values which will be used in Neat._
- $grid-defaults {`Object`} [`('mobile-s': 320px, 'mobile-xl': 657px, 'tablet-p': 768px, 'tablet-l': 1024px, 'desktop': 1440px)`] - _Default values which will be used in Neat._
- $grid-class-col {`String`} [`is-col`] - _Column class namespace._
- $grid-offset {`String`} [`offset`] - _Offset class namespace._

### Output

In combination with the Sass map for all major breakpoints, a specific mixin creates our markup classes which has the following structure: 
- `.{$grid-class-col}-[namesace]-[number]` - _for a column that covers a specific number of columns (e.g. 1-12 by default)_
- `.{$grid-class-col}-[namespace]-{$grid-offset}-[number]` - _for pushing a col a specific number of columns (e.g. 1-11 by default)_

### Modifier Classes

You can add the following modifiers to `u-grid-row|is-grid-row`:
- is-collapsed - _Delete the margin on the left (can be set via `settings.gridCollapsed`)_
- is-equal-height - _Add flex box styles to support equal heights for the columns_

### Usage Examples
- `is-col-mobile-s-12 is-col-mobile-xl-6 is-col-tablet-p-4 is-col-tablet-p-offset-4 is-col-tablet-l-3 is-col-tablet-l-offset-0`

-------------

## Fields

### Grid Row

- settings.gridCollapsed {`Boolean`} - _Delete the margin to the left._ 
- settings.gridClasses {`String`} - _Modifier classes like `is-equal-height`._ 

### Grid Col

- colClasses {`String`} - _Column and offset classes._

