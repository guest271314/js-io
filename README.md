# js-io
Specify I/O for ECMAScript

There's no I/O. No `stdin`, `stdout`, `sterr`. Each JavaScript context is a unique process, capable of 
handling standard input, standard output, standard error. Write out a function to do that, simple enough to be 
implemented in any engine, runtime, interpreter, context the host decides. It's optional. The goal is compatibility.
Same signature.

```javascript
read(buffer, options = {})
``` 

Read bytes from `stdin` into `buffer`, `TypedArray`. Bring your own `buffer`. `min`, `max`, `fd` (`0`, `2`,..., e.g., `3`, custom I/O)  options. Asynchrously. Synchromously. 

```javascript
write(buffer, options = {})
```
Write `buffer` `TypedArray` bytes to `stdout`. `fd` (`1`, `2`,...) options. Asynchronously. Synchronusly.

Pretty simple so far. 
