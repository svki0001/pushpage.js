# pushpage.js

ES6 framework for dynamic stacked popups.

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/svki0001/pushpage.js/blob/master/LICENSE)

## Installation

Download `dist/pushpage.min.js` and include the script on your page like shown below.

## Usage

```html
<script src="pushpage.min.js"></script>

<div id="container"></div>

<script>
let Container = document.getElementById('container');

let pp1 = new Pushpage({
    container: Container,
    fileUrl: 'pushpages/pp1.html',
    urlParamName: 'pp1'
});
let pp2 = new Pushpage({
    container: Container,
    fileUrl: 'pushpages/pp2.html',
    urlParamName: 'pp2'
});
let ppscript = new Pushpage({
    container: Container,
    fileUrl: 'pushpages/ppscript.html',
    urlParamName: 'ppscript',
    scriptUrl: 'demo.js'
});

let pa = [pp1, pp2, ppscript];

let pc = new PushpageCollection(pa);
</script>
```

The following options are available to pass to the `Pushpage` object.

Option             | Description              
-------------------|-------------------------------------------------------------------------------------------------
`container`        | The DOM element in which the pushpage will be appended.
`fileUrl`          | The URL for pushpage template file (.html).
`urlParamName`     | The pushpage target url paramater.
`scriptUrl`        | The URL for the scripts which will be executed after opening a pushpage. Can be string or array.

## License

MIT
