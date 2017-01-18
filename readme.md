Image masking using canvas and jQuery
=====================================

This repository is a jQuery-based fork of [codepo8's image masking solution](https://github.com/codepo8/canvas-masking). The code has been abstracted into a function called `applyMasks()` which can be used in whatever context you require, for example applying masks on asynchronously loaded images.

## Default usage:

```javascript
$(document).ready(function () {
  applyMasks();
});
```

By default the function loops through all `img` tags that have the `mask` class and applies the alpha mask specified in each image's `data-mask` attribute like so:

```xml
<img src="red-panda.jpg" alt="Red panda" class="mask" data-mask="centerblur.png">
```
This will take the `centerblur.png` file and apply it as a mask to `red-panda.jpg` - in effect taking the alpha of each pixel and change the alpha of the original pixel to that.

You can see it in action here: http://codepo8.github.io/canvas-masking/

## Configuration

The function takes only one parameter - a jQuery object to loop through. This allows applying the masks to selected elements only.

```javascript
applyMasks($('.masked'));
```

***

Many thanks to [codepo8](https://github.com/codepo8) for the original script.