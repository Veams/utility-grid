# Grid

Bourbon Neat provides a simple grid system, which you can use in your projects. 

With `u-grid` there is implemented a mobile first class based system which is like Bootstrap or Foundation, but you are also flexible enough to just use mixins in your Sass or SCSS files. 

## Requirements
- Bourbon Neat in Beta => http://neat.bourbon.io/ => `bower install neat#v2.0.0.beta.1 --save-dev`
- wrapWith helper => https://www.npmjs.com/package/mangony-hbs-helper-wrap-with => `npm install mangony-hbs-helper-wrap-with --save-dev`

### Documentation
- Bourbon Neat: http://thoughtbot.github.io/neat-docs/2-0-0-beta-1/ 

## Usage

In general `u-grid.scss` generates a set of grid column classes using namespaces: 
- `$grid-class-col`: "`is-col`"
- `$grid-offset`: "`offset`"

In combination with a Sass map for all major breakpoints, a specific mixin creates our markup classes which has the following structure: 
- .{$grid-class-col}-[namespace]-[number] - for a column that covers a specific number of columns (e.g. 1-12 by default)
- .{$grid-class-col}-[namespace]-{$grid-offset}-[number] - for pushing a col a specific number of columns (e.g. 1-11 by default)

### Modifier Classes

You can add the following modifiers to `u-grid-row`:
- `is-collapsed` - Delete the margin on the left (can be set via `settings.gridCollapsed`)
- `is-equal-height` - Add flex box styles to support equal heights for the columns

### Usage Examples
- `is-col-mobile-s-12 is-col-mobile-xl-6 is-col-tablet-p-4 is-col-tablet-p-offset-4 is-col-tablet-l-3 is-col-tablet-l-offset-0`