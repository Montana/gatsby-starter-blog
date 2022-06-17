---
title: chachi loves doomscrolling 
date: "2022-06-16T22:40:32.169Z"
description: Endless Doomscrolling, hang in there, the world gets worse!
---

## Is floating point math broken?

Consider the following code:

```r
0.1 + 0.2 == 0.3  ->  false
0.1 + 0.2         ->  0.30000000000000004
```
Why do these inaccuracies happen? The answer is simlpe, all base-N systems share this problem with surgical precision. Another example is if I were to run this snippet of JavaScript in my DevConsole: 

```javascript
function test() {
  var x = 0.1 * 0.2;
  document.write(x);
}
test();
```

The result would be `0.020000000000000004`. When dealing with 32 or 64 bit floats, you should use `toPrecision(7)` and `toPrecision(15)` for best results.

_chachi_
