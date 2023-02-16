# Notch CSS

This is a small project started because I belive in progress web apps or PWAs. I always struggled with the right top and bottom spacing when designing or developing. This repo and [demo](https://nikaocreatives.github.io/notch-css/) help me with that issue.

This repo contains one `index.html` file with some CSS that allows you to set a header and footer that will adjust on each device and set the right padding to get out of the way of those notches. This can be achieved by using `env()` in CSS, but I hope the demo can provide some clarity when `env()` is being used and not being used.

## The CSS

Its not much, but helps tremendously. You can incorporate this into your header and foot code or just use the classes provided.

```CSS
:root {
    --sat: env(safe-area-inset-top);
    --sar: env(safe-area-inset-right);
    --sab: env(safe-area-inset-bottom);
    --sal: env(safe-area-inset-left);
}

body {
    padding:
        var(--sat) var(--sar) var(--sab) var(--sal);
    padding-top: var(--sat);
    padding-bottom: var(--sab);
}

.notch--header {
    position: fixed;
    top: 0px;
    width: 100%;
    height: auto;
    padding-top: var(--sat);
    z-index: 100;
}

.notch--footer {
    position: fixed;
    bottom: 0px;
    width: 100%;
    height: auto;
    padding-bottom: var(--sab);
    z-index: 100;
}
```

## The Demo

This demo really helps me as a designer as I'm not sure on the safe areas all the time. It can also can help developers identify when something gets a safe area like safari mobile vs adding a website to your homescreen.

Check out the demo [here](https://nikaocreatives.github.io/notch-css/).

## Questions

Reach out with quesitions or comments via [twitter](https://twitter.com/chasturansky) or my [website](http://turansky.net/?utm_source=github&utm_medium=readme&utm_campaign=notch-css).
