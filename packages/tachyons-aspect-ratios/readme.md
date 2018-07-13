# tachyons 5.0.0-1

Functional CSS for humans

### Stats

873 | 52 | 84
---|---|---
bytes | selectors | declarations

## Installation

#### With [npm](https://npmjs.com)

```
npm install --save-dev tachyons
```

Learn more about using css installed with npm:
* https://webpack.github.io/docs/stylesheets.html
* https://github.com/defunctzombie/npm-css

#### With Git

http:
```
git clone https://github.com/tachyons-css/tachyons
```

ssh:
```
git clone git@github.com:tachyons-css/tachyons.git
```

## Usage

#### Using with [Postcss](https://github.com/postcss/postcss)

Import the css module

```css
@import "tachyons";
```

Then process the css using the [`tachyons-cli`](https://github.com/tachyons-css/tachyons-cli)

```sh
$ npm i -g tachyons-cli
$ tachyons path/to/css-file.css > dist/t.css
```

#### Using the css

##### CDN
The easiest and most simple way to use the css is to use the cdn hosted version. Include it in the head of your html with:

```
<link rel="stylesheet" href="http://unpkg.com/tachyons@5.0.0-1/css/tachyons.min.css" />
```

##### Locally
The built css is located in the `css` directory. It contains an unminified and minified version.
You can either cut and paste that css or link to it directly in your html.

```html
<link rel="stylesheet" href="path/to/module/css/tachyons">
```

#### Development

The source css files can be found in the `src` directory.
Running `$ npm start` will process the source css and place the built css in the `css` directory.

## The css

```css
/*!!!

# ASPECT RATIOS

This is for fluid media that is embedded from third party sites like youtube, vimeo etc.
Wrap the outer element in aspect-ratio and then extend it with the desired ratio i.e
Make sure there are no height and width attributes on the embedded media.
Adapted from: https://github.com/suitcss/components-flex-embed

### Docs

https://tachyons.io/docs/layout/aspect-ratios

### Base

- aspect-ratio = aspect ratio

### Modifiers

- `--16x9` = 16x9
- `--9x16` = 9x16
- `--4x3` = 4x3
- `--3x4` = 3x4
- `--6x4` = 6x4
- `--4x6` = 4x6
- `--8x5` = 8x5
- `--5x8` = 5x8
- `--7x5` = 7x5
- `--5x7` = 5x7
- `--1x1` = 1x1
- `--object` = object

### Media Query Extensions

- `-s` = small
- `-m` = medium
- `-l` = large

### Example

```html
<div class="aspect-ratio aspect-ratio--16x9">
<iframe class="aspect-ratio--object"></iframe>
</div>
```
*/
.aspect-ratio { height: 0; position: relative; }
.aspect-ratio--16x9 { padding-bottom: 56.25%; }
.aspect-ratio--9x16 { padding-bottom: 177.77%; }
.aspect-ratio--4x3 { padding-bottom: 75%; }
.aspect-ratio--3x4 { padding-bottom: 133.33%; }
.aspect-ratio--6x4 { padding-bottom: 66.6%; }
.aspect-ratio--4x6 { padding-bottom: 150%; }
.aspect-ratio--8x5 { padding-bottom: 62.5%; }
.aspect-ratio--5x8 { padding-bottom: 160%; }
.aspect-ratio--7x5 { padding-bottom: 71.42%; }
.aspect-ratio--5x7 { padding-bottom: 140%; }
.aspect-ratio--1x1 { padding-bottom: 100%; }
.aspect-ratio--object { position: absolute; top: 0; right: 0; bottom: 0; left: 0; width: 100%; height: 100%; z-index: 100; }
@media screen and (min-width: 30em) {
 .aspect-ratio-s { height: 0; position: relative; }
 .aspect-ratio--16x9-s { padding-bottom: 56.25%; }
 .aspect-ratio--9x16-s { padding-bottom: 177.77%; }
 .aspect-ratio--4x3-s { padding-bottom: 75%; }
 .aspect-ratio--3x4-s { padding-bottom: 133.33%; }
 .aspect-ratio--6x4-s { padding-bottom: 66.6%; }
 .aspect-ratio--4x6-s { padding-bottom: 150%; }
 .aspect-ratio--8x5-s { padding-bottom: 62.5%; }
 .aspect-ratio--5x8-s { padding-bottom: 160%; }
 .aspect-ratio--7x5-s { padding-bottom: 71.42%; }
 .aspect-ratio--5x7-s { padding-bottom: 140%; }
 .aspect-ratio--1x1-s { padding-bottom: 100%; }
 .aspect-ratio--object-s { position: absolute; top: 0; right: 0; bottom: 0; left: 0; width: 100%; height: 100%; z-index: 100; }
}
@media screen and (min-width: 48em) {
 .aspect-ratio-m { height: 0; position: relative; }
 .aspect-ratio--16x9-m { padding-bottom: 56.25%; }
 .aspect-ratio--9x16-m { padding-bottom: 177.77%; }
 .aspect-ratio--4x3-m { padding-bottom: 75%; }
 .aspect-ratio--3x4-m { padding-bottom: 133.33%; }
 .aspect-ratio--6x4-m { padding-bottom: 66.6%; }
 .aspect-ratio--4x6-m { padding-bottom: 150%; }
 .aspect-ratio--8x5-m { padding-bottom: 62.5%; }
 .aspect-ratio--5x8-m { padding-bottom: 160%; }
 .aspect-ratio--7x5-m { padding-bottom: 71.42%; }
 .aspect-ratio--5x7-m { padding-bottom: 140%; }
 .aspect-ratio--1x1-m { padding-bottom: 100%; }
 .aspect-ratio--object-m { position: absolute; top: 0; right: 0; bottom: 0; left: 0; width: 100%; height: 100%; z-index: 100; }
}
@media screen and (min-width: 60em) {
 .aspect-ratio-l { height: 0; position: relative; }
 .aspect-ratio--16x9-l { padding-bottom: 56.25%; }
 .aspect-ratio--9x16-l { padding-bottom: 177.77%; }
 .aspect-ratio--4x3-l { padding-bottom: 75%; }
 .aspect-ratio--3x4-l { padding-bottom: 133.33%; }
 .aspect-ratio--6x4-l { padding-bottom: 66.6%; }
 .aspect-ratio--4x6-l { padding-bottom: 150%; }
 .aspect-ratio--8x5-l { padding-bottom: 62.5%; }
 .aspect-ratio--5x8-l { padding-bottom: 160%; }
 .aspect-ratio--7x5-l { padding-bottom: 71.42%; }
 .aspect-ratio--5x7-l { padding-bottom: 140%; }
 .aspect-ratio--1x1-l { padding-bottom: 100%; }
 .aspect-ratio--object-l { position: absolute; top: 0; right: 0; bottom: 0; left: 0; width: 100%; height: 100%; z-index: 100; }
}
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Authors

* [mrmrs](http://mrmrs.io)
* [johno](http://johnotander.com)

## License

ISC
