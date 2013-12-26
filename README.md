![status](https://secure.travis-ci.org/wearefractal/gulp-coffee.png?branch=master)

## Information

<table>
<tr> 
<td>Package</td><td>gulp-coffee</td>
</tr>
<tr>
<td>Description</td>
<td>Compiles CoffeeScript</td>
</tr>
<tr>
<td>Node Version</td>
<td>>= 0.4</td>
</tr>
</table>

## Usage

```javascript
var coffee = require('gulp-coffee');

gulp.task('coffee', function() {
  gulp.src('./src/*.coffee')
    .pipe(coffee({bare: true}))
    .pipe(gulp.dest('./public/'))
});
```

### Error handling

```javascript
var coffee = require('gulp-coffee');

var coffeeStream = coffee({bare: true});

// Catch gulp-coffee error
coffeeStream.on('error', function(err) {
    if(err) console.log(''+err);
});

gulp.task('coffee', function() {
  gulp.src('./src/*.coffee')
    .pipe(coffeeStream)
    .pipe(gulp.dest('./public/'))
});
```

## Options

The options object supports the same options as the standard CoffeeScript compiler 

## LICENSE

(MIT License)

Copyright (c) 2013 Fractal <contact@wearefractal.com>

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
