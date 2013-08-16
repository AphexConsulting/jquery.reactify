# jquery.reactify

Make browser click events trigger immediately on iOS and Android.

## Installing

1. Clone the repository (git clone https://github.com/AphexConsulting/jquery.reactify)
1. Place `jquery.reactify.js` to your project's JavaScript folder
1. Add `<script type="text/javascript" src="js/jquery.reactify.js"></script>` to your HTML
1. Add a script that enables reactify with jQuery: $(selector).reactify();

## Dependencies

Requires jQuery 1.9.0 or newer.

## Example

```JavaScript
$('input[type=button]').reactify();
```

## Known issues

On Android in some situations the tocuhstart event is not always fired. For some reason running the following code before registering the fastlongclick events solves the issue. If you know a fix for this problem, please contact me.

```JavaScript
var events = 'mousedown touchstart mouseup touchend click mousemove touchmove touchcancel mouseout';
$(document).off(events);
$(document).on(events, function(e) { });
```

# License

The library is licensed under the MIT-license:

> Copyright (C) 2012 Aphex Consulting Oy

> Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

> The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
