<!--
[![A great header image you designed, or collaborated on with a designer you work with. It’ll look best when it’s 728px wide, @2x for hi-dpi devices.](preview.png)](https://github.com/kennethormandy/hanging-punctuation)

***
-->

# Hanging Punctuation

A polyfill for proper [hanging punctuation](http://www.w3.org/TR/css-text-3/#hanging-punctuation) in CSS.

Soon, you’ll be able to apply proper hanging punctuation in CSS without any JavaScript:

```css
p {
  hanging-punctuation: first;
}

html[lang="zh-Hans"] {
  text-align: justify;
  hanging-punctuation: allow-end;
}
```

In the meantime, this [Stylefill](https://github.com/nathanford/stylefill/) polyfills the missing features through the exact same CSS. Now, the first glyph only hangs if it is at the beginning of a line, correcting

```
“Lorem  ipsum  dolor  sit  amet, consectetuer
adipiscing elit. Ut a sapien alt,” they said,
“Purus  molestie  dolor. Integer  quis eros ut
erat posuere dictum.”
```

to this:

```
“Lorem  ipsum  dolor  sit  amet, consectetuer
 adipiscing elit. Ut a sapien alt,” they said,
“Purus  molestie  dolor. Integer  quis eros ut
 erat posuere dictum.”
```

## Getting started

Hanging Punctuation is a [Stylefill](https://github.com/nathanford/stylefill/), meaning you only need to interact with this library through your CSS, and browsers that already support the `hanging-punctuation` property won’t use this polyfill.

To install Hanging Punctuation, add it to your project or use the package manager and build tool of your choice.

<!--

##### Manually

-->

##### With npm

```bash
npm install kennethormandy/hanging-punctuation
```

Now it’s ready to include through your task runner orbuild tool, or you may just reference the files in your HTML:

```html
<script src="node_modules/hanging-punctuation/hanging-punctuation.min.js"></script>
```

<!--

##### With Component

```bash
component install kennethormandy/hanging-punctuation
```

##### With Bower

```bash
bower install hanging-punctuation
```

-->

## Contributing

Thanks for considering contributing! There’s information about how to [get started with Default here](CONTRIBUTING.md).

## License

[The MIT License (MIT)](LICENSE.md)

Copyright © 2014 [Kenneth Ormandy](http://kennethormandy.com) & [Chloi Inc.](http://chloi.io)

```
