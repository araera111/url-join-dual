# url-join-dual

[`url-join-dual`](https://github.com/araera111/url-join-dual) is a library that joins all arguments together and normalizes the resulting URL. This library has been enhanced to be used with both ESM and CommonJS. It is based on the [url-join](https://github.com/jfromaniello/url-join) library.

## Installation

```bash
npm install url-join-dual
```

## Usage

```javascript
import urlJoin from 'url-join-dual';

const fullUrl = urlJoin('http://www.google.com', 'a', '/b/cd', '?foo=123', '&bar=456', '#heading-1');

console.log(fullUrl.toString()); // 'http://www.google.com/a/b/cd?foo=123&bar=456#heading-1'
```

For usage with CommonJS:

```javascript
const urlJoin = require('url-join-dual');

const fullUrl = urlJoin('http://www.google.com', 'a', '/b/cd', '?foo=123', '&bar=456', '#heading-1');

console.log(fullUrl.toString()); // 'http://www.google.com/a/b/cd?foo=123&bar=456#heading-1'
```

## You might not need this library

This library was originally created before the [URL API](https://developer.mozilla.org/en-US/docs/Web/API/URL_API) was standardized and widely available in popular runtimes such as browsers and Node.js. Depending on your use-case you might want to consider using the standardized API over this library.

### In the Browser

For example, the equivalent code for the above example would look as follows when using the URL API:

```javascript
const fullUrl = new URL('http://www.google.com');
```

## Author

KATO_Yuumin

## License

MIT