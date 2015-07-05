<div align="center">
  <a href="http://github.com/flyjs/fly">
    <img width=200px  src="https://cloud.githubusercontent.com/assets/8317250/8430194/35c6043a-1f6a-11e5-8cbd-af6cc86baa84.png">
  </a>
</div>

> [Fly](https://github.com/flyjs/fly) plugin for [PostCSS](https://github.com/postcss/postcss)
>
[![][fly-badge]][fly] ![][mit-badge]

## Usage

### Install

```shell
$ npm install -D fly-postcss
```

### Example

```js
exports.postcss = function* () {
  yield this
    .source('src/*.css')
    .postcss([
        require('cssnext')(),
        require('cssnano')()
    ], {
        from: 'a.css',
        to: 'a.out.css'
    })
    .target('dist')
}
```

## License

[MIT](http://opensource.org/licenses/MIT) © [Masaaki Morishita][author]


[author]: https://github.com/morishitter

[fly]: https://www.github.com/flyjs/fly

[fly-badge]: https://img.shields.io/badge/fly-JS-05B3E1.svg?style=flat-square
[mit-badge]: https://img.shields.io/badge/license-MIT-444444.svg?style=flat-square

