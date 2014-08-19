skrollr-parallax-demo
=====================

This is a simple [skrollr](//github.com/Prinzhorn/skrollr) parallax demo to help illustrate the concept outlined [here](//github.com/Prinzhorn/skrollr/issues/576#issuecomment-51730312) used to remedy the seemingly arbitrary cutoff of page content in mobile, and particularly iOS devices.

This demo consists of:

- A [**'before' page**](//paskainos.github.io/skrollr-parallax-demo/before.html) which is simply a clone of [the classic parallax example](http://prinzhorn.github.io/skrollr/examples/classic.html) with some additional page content added within `#skrollr-body` to reproduce the seemingly arbitrary cutoff on mobile devices.
- An [**'after' page**](//paskainos.github.io/skrollr-parallax-demo/after.html), identical to the before page, but which simply adds this keyframe information - `data-bottom="top: 0%;" data-top="top: 0%;"` - to the last element (the `#done` element in this case) within `#skrollr-body` to identify the end of (`#skrollr-body`) [relative page content](//github.com/Prinzhorn/skrollr#relative-mode-or-viewport-mode) for skrollr, particularly in mobile, thus helping skrollr properly calculate mobile page content height and in turn 'fixing' the seemingly arbitrary cutoff.

##NOTE:##
The keyframe markup effects the document length. For instance, changing the above keyframe markup to `data-bottom-top="top: 0%;" data-top-bottom="top: 0%;"` will add 100% viewport height to the total document height, in turn causing the actual page bottom to scroll up out of view.
