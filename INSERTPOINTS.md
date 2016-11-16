## Usage

### Include: Page

``` hbs
{{! @INSERT :: START @id: grid, @tag: utility-partial }}
{{#wrapWith "u-grid-row"}}
    {{#wrapWith "u-grid-col" colClasses="is-col-mobile-s-1" }}
        Col 1
    {{/wrapWith}}
    {{#wrapWith "u-grid-col" colClasses="is-col-mobile-s-11" }}
        Col 11
    {{/wrapWith}}
{{/wrapWith}}
{{! @INSERT :: END }}
```

### Include: SCSS

``` scss
// @INSERT :: START @tag: scss-import //
@import "helpers/_h-grid";
@import "utilities/_u-grid";
// @INSERT :: END
```