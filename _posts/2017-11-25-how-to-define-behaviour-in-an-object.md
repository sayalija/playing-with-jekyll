---
layout: post
title: How to define behaviour in an object?
url: how-to-define-behaviour-in-an-object
category: post
---


#### Defining Behaviour In An Object

If you have read the post [Why Objects?](why_objects), then you will understand the need for tying data and behaviour together. If you haven't read it, please do so before you proceed any further.

Kavita and John have understood that it is necessary to tie data and behaviour together. One manner of doing it is to define the behaviour when you create the object.

```javascript
var areaOfSquare=function() {
  return this.length * this.length;
}

var createSquare=function(length) {
  let square={length:length}
  square.area=areaOfSquare;
  return square;
}

exports.createSquare=createSquare;
```

This can be used very easily now.
