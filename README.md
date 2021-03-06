# sha.js

Streamable SHA1 hash in pure javascript.

[![build status](https://secure.travis-ci.org/dominictarr/sha.js.png)](http://travis-ci.org/dominictarr/sha.js)
[![testling badge](https://ci.testling.com/dominictarr/sha.js.png)](https://ci.testling.com/dominictarr/sha.js)

## Example

``` js
var Sha1 = require('sha.js')
var h = new Sha1().update('abc', 'utf8').digest('hex')
console.log(h) //a9993e364706816aba3e25717850c26c9cd0d89d
```

## Note

Note, this doesn't actually implement a stream, but wrapping this in a stream is trivial.
but is does update incrementally, so you can hash things larger than ram, and also, since it reuses
the typedarrays, it uses a constant amount of memory (except when using base64 or utf8 encoding,
see code comments)

## Acknowledgements

This work is derived from Paul Johnston's ["A JavaScript implementation of the Secure Hash Algorithm"]
(http://pajhome.org.uk/crypt/md5/sha1.html)

# TODO

* sha256 (and similar)
* md5

(and any other similar hashes that are close to this model)

## License

MIT
