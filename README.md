# bip21

[![build status](https://secure.travis-ci.org/bitcoinjs/bip21.png)](http://travis-ci.org/bitcoinjs/bip21)
[![Version](http://img.shields.io/npm/v/bip21.svg)](https://www.npmjs.org/package/bip21)

A [BIP21](https://github.com/bitcoin/bips/blob/master/bip-0021.mediawiki) compatible URL encoding library.


## Example

``` javascript
var bip21 = require('bip21')

var decoded = bip21.decode('actinium:PEwr8xxbULYLzNggPMQ1fT5RD8irnEZ9gS?amount=20.3&label=Foobar')

console.log(decoded)
// { address: 'PEwr8xxbULYLzNggPMQ1fT5RD8irnEZ9gS',
//   options: {
//     amount: 20.3,
//     label: 'Foobar' }
// }
//
// WARNING: Remember to error check the `.address`!

console.log(bip21.encode('PEwr8xxbULYLzNggPMQ1fT5RD8irnEZ9gS'))
// => actinium:PEwr8xxbULYLzNggPMQ1fT5RD8irnEZ9gS

console.log(bip21.encode('PEwr8xxbULYLzNggPMQ1fT5RD8irnEZ9gS', {
	amount: 20.3,
	label: 'Foobar'
}))
// => actinium:PEwr8xxbULYLzNggPMQ1fT5RD8irnEZ9gS?amount=20.3&label=Foobar
```


## License [MIT](LICENSE)
