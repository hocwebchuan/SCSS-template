# SCSS TEMPLATE
This template is a basic template use for SCSS project.

## Table of Contents
- [Folder Structure](#folder-structure)
- [Available Scripts](#available-scripts)
- [Some helpful modules](#Some-helpful-modules)
- [Something Missing?](#something-missing)

## Folder Structure

After download source code, your project should look like this:

```
SCSS-template/
  css/
    style.css
  scss/
    base/
      mixins/
        _breakpoints.scss
        _default.scss
        _flexbox.scss
        _hover.scss
        _misc.scss
        _module.scss
        _transform.scss
      _base.scss
      _mixins.scss
      _reset.scss
      _variables.scss
    components/
      vendor/
        _sample_lightbox.scss
      _button.scss
      _form.scss
      _headline.scss
    layout/
      _aside.scss
      _footer.scss
      _grid.scss
      _header.scss
      _main.scss
      _nav.scss
    pages/
      _contact.scss
      _home.scss
    style.scss
  package.json
  package-lock.json
  README.md
```

## Available Scripts
In the project directory, follow these steps to setup SASS auto compile the CSS file:

```sh
npm install
npm install node-sass
npm run scss
```

## Some helpful modules
### Border position
```css
@mixin bdr-position($pos,$radius) {
    border-radius: 0;
    @if $pos == 'top' {
        border-#{$pos}-left-radius: $radius;
        border-#{$pos}-right-radius: $radius;
    }@else if $pos == 'bottom' {
        border-#{$pos}-left-radius: $radius;
        border-#{$pos}-right-radius: $radius;
    }@else if $pos == 'right' {
        border-bottom-#{$pos}-radius: $radius;
        border-top-#{$pos}-radius: $radius;
    }@else if $pos == 'left' {
        border-bottom-#{$pos}-radius: $radius;
        border-top-#{$pos}-radius: $radius;
    }
}
```

Easy to use:
```css
bdr-position(top,5px)
```

It will compile to:
```css
border-top-left-radius: 5px;
border-top-right-radius: 5px;
```

### Position absolute
```css
@mixin position($pos,$y,$x) {
    position: absolute;
    @if $pos == 'tl' {
        left: $x;
        top: $y;
    }@else if $pos == 'tr' {
        right: $x;
        top: $y;
    }@else if $pos == 'bl' {
        left: $x;
        bottom: $y;
    }@else if $pos == 'br' {
        right: $x;
        bottom: $y;
    }
}
```

Easy to use:
```css
position(tl,10px,20px)
```

It will compile to:
```css
position: absolute;
left: 20px;
top: 10px;
```

## Something missing?

If you have any problems, [let me know](https://github.com/hocwebchuan/SCSS-template/issues).<br>
Thanks for using it!