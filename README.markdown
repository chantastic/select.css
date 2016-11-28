# select.css

A stupid, styleable, scalable class for selects.

## Why?

I wanted a cross-browser select that I could easily style and npm install.

This isn't clever.
It controls the shape and doesn't try to hard about override the browser's
default disclosure button.

![ff pre-35 and ff 35](https://cloud.githubusercontent.com/assets/658360/5458763/c354e8da-8509-11e4-8c52-4b00a469c21b.png)

FF<34 and FF35+

![ie9 and ie10](https://cloud.githubusercontent.com/assets/658360/5458760/bf0807b2-8509-11e4-82cf-35c00ae93a60.png)

IE9 and IE10 (with `ie9-select.css`)


## Prior art

I borrowed techniques from [wtfforms](http://wtfforms.com/),
[mailchimp](https://mailchimp.com/),
and [foundation](http://foundation.zurb.com/).

It's been 2 years now. So they could have totally moved on.

## Install

#### NPM

`npm install select.css@0.0.1`

#### Script tag

`<link rel="stylesheet" href="https://unpkg.com/select.css@0.0.1" />`

## Use

```html
<select class="select">
  ...  
</select>
```

### Theming

BYOTheme.

The base `.select` class sets a few colors, just in case you really don't want to think about anything.

In most cases, you'll probably color the selects to match your app.
Themes look like this:

```css
.select {
  background-color:#fcfcfc;
  border-color:#d7d7d7;
  color:#3f3f3f;
}
.select:hover {
  background-color:#eee;
  border-color:#c4c4c4;
}
```

### IE9

Include the `ie9-select.css` file if you need IE9 support.
It just changes a couple styles to make the default disclosure button fall in a better spot.

#### DON'T SET `background`

It's important not to set `backrgound`.
It'll remove the little disclosure chevron.
If you want to change the `background-color`, set `background-color`.

## Code

This is all the code there is.

```css
/*! select.css */
.select{
position:relative;
background-image:url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZlcnNpb249IjEuMSIgeD0iMTJweCIgeT0iMHB4IiB3aWR0aD0iMjRweCIgaGVpZ2h0PSIzcHgiIHZpZXdCb3g9IjAgMCA2IDMiIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDYgMyIgeG1sOnNwYWNlPSJwcmVzZXJ2ZSI+PHBvbHlnb24gcG9pbnRzPSI1Ljk5MiwwIDIuOTkyLDMgLTAuMDA4LDAgIi8+PC9zdmc+);
background-position:right center;
background-color:transparent;
background-repeat:no-repeat;
background-size:2em auto;
display:inline-block;
vertical-align:middle;
cursor:pointer;
-webkit-appearance:none;-moz-appearance:none;appearance:none;
border-radius:.25em;
border-width:1px;
border-style:solid;
height:2em;
font-size:1em;
padding:0 2em 0 .5em;
/* default theme */
background-color:#fcfcfc;
border-color:#d7d7d7;
color:#3f3f3f;
}
```
