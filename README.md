&lt;x-html&gt;
==============

`<x-html>` is a custom element that lets you load HTML partials into your Web Components

If you have this:

```javascript
var model = {
  appdata: {
    username: "World",
    html: "<h1>Hello {{ username }}</h1>"
  }  
}
```

You can put it on screen with this:

```html
<template bind="{{ appdata }}">
  <x-html content="{{ html }}"></x-html>
</template>
```

### Features

Your HTML partials can contain:
 - regular HTML
 - inline scripts using `<script>//JS code here</script>`
 - inline styles using `<style>/*CSS code here*/</style>`
 - external stylesheets using `<link rel="stylesheet" href="path/to/file.css">`, with `href` value relative to the document
 - HTML imports using `<link rel="import" href="path/to/file.html">`, with `href` value relative to the document

Of course, the 2-way data binding provided by works within your partials as desired.

### Usage

Load HTML partial from a string:

```
<x-html content="{{ var }}"></x-html>
<!-- where {{ var }} equals "<b>some</b> HTML" -->
```

Load HTML partial from a URL:

```
<x-html content="{{ var }}"></x-html>
<!-- where {{ var }} equals "./path/to/file.html", a path relative to the document that must start with / or ./ -->
```

More advanced examples can be found in [examples](https://github.com/PuppetJs/x-html/blob/master/examples) directory.

### Dependencies

`<x-html>` is dependent on [Polymer](http://www.polymer-project.org/) as a polyfill for Web Components APIs. In
future, it will be library-agnostic.

### Changelog

#### v0.0.20131118

Started its own repo: [PuppetJs/x-html](https://github.com/PuppetJs/x-html)
