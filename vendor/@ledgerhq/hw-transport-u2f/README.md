<img src="https://user-images.githubusercontent.com/211411/34776833-6f1ef4da-f618-11e7-8b13-f0697901d6a8.png" height="100" />

[Github](https://github.com/LedgerHQ/ledgerjs/),
[Ledger Devs Slack](https://ledger-dev.slack.com/)

## @ledgerhq/hw-transport-u2f

Allows to communicate with Ledger Hardware Wallets.

**[Web]** **(U2F)** (legacy but reliable) – FIDO U2F api. [check browser support](https://caniuse.com/u2f).

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

#### Table of Contents

-   [TransportU2F](#transportu2f)
    -   [Examples](#examples)
    -   [exchange](#exchange)
        -   [Parameters](#parameters)
    -   [setScrambleKey](#setscramblekey)
        -   [Parameters](#parameters-1)
    -   [setUnwrap](#setunwrap)
        -   [Parameters](#parameters-2)
    -   [open](#open)
        -   [Parameters](#parameters-3)

### TransportU2F

**Extends Transport**

U2F web Transport implementation

#### Examples

```javascript
import TransportU2F from "@ledgerhq/hw-transport-u2f";
...
TransportU2F.create().then(transport => ...)
```

#### exchange

Exchange with the device using APDU protocol.

##### Parameters

-   `apdu` **[Buffer](https://nodejs.org/api/buffer.html)** 

Returns **[Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;[Buffer](https://nodejs.org/api/buffer.html)>** a promise of apdu response

#### setScrambleKey

##### Parameters

-   `scrambleKey` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 

#### setUnwrap

##### Parameters

-   `unwrap` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

#### open

static function to create a new Transport from a connected Ledger device discoverable via U2F (browser support)

##### Parameters

-   `_` **any** 
-   `_openTimeout` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)**  (optional, default `5000`)

Returns **[Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;[TransportU2F](#transportu2f)>** 
