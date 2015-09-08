# sodium-signatures

Sodium signatures that works in node and in the browser

```
npm install sodium-signatures
```

## Usage

``` js
var signatures = require('sodium-signatures')

var keys = signatures.keyPair()
var message = new Buffer('a message')

var signature = signatures.sign(message, keys.secretKey)
var verified = signatures.verify(message, signatures, keys.publicKey)

console.log('message was verified', verified)
```

## API

#### `keys = signatures.keyPair()`

Generate a public key and a secret key.

#### `signature = signature.sign(message, secretKey)`

Sign a message.

#### `verified = signature.verify(message, signature, publicKey)`

Verify a message and signature.

## License

MIT