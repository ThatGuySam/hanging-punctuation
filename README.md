> _Hanging punctuation_ prevents quotations and other marks from taking a bite out of the crisp left edge of a text block. Make a clean edge by pushing the quotation marks into the margin.<br/>
> &nbsp;&nbsp;&nbsp;&nbsp;—Ellen Lupton, _Thinking with Type, 2<sup>nd</sup> Revised and Expanded Edition_

# Hanging Punctuation

A polyfill for proper [hanging punctuation](http://www.w3.org/TR/css-text-3/#hanging-punctuation) in CSS.

The `hanging-punctuation` property should be part of CSS in the future, but no browser supports in yet. In the meantime, this [Stylefill](https://github.com/nathanford/stylefill/) polyfills the missing features through the exact same CSS:

```css
p {
  hanging-punctuation: first;
  /* Dynamically hang punctuation
     on the left margin. */
}

html[lang="zh-Hans"] {
  text-align: justify;
  hanging-punctuation: allow-end;
  /* Allow ending punctuation
     to hang even when justified. */
}
```

Now, the first glyph only hangs if it is at the beginning of a line. This corrects

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

Now it’s ready to include through your task runner or build tool, or you may just reference the files in your HTML:

```html
<script src="node_modules/hanging-punctuation/hanging-punctuation.min.js"></script>
```

##### With Component

```bash
component install kennethormandy/hanging-punctuation
```

##### With Bower

```bash
bower install hanging-punctuation
```

## Running locally

To run the tests locally:

```bash
git clone https://github.com/kennethormandy/hanging-punctuation
npm install
npm test
# Now visit http://127.0.0.1:8080/test
```

## Contributing

Thanks for considering contributing! There’s information about how to [get started with Hanging Punctuation here](CONTRIBUTING.md).

## License

[The MIT License (MIT)](LICENSE.md)

Copyright © 2014 [Kenneth Ormandy](http://kennethormandy.com) & [Chloi Inc.](http://chloi.io)
