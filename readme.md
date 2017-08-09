## gulp-timestamp-css-url

a plugin for gulp.js to replace version for images in css files,the version should be file's md5 or time stamp;

## Installation

```bash
npm install gulp-timestamp-css-url
```

## Usage

```js
var makeUrlVer = require('gulp-timestamp-css-url');

gulp.task('stylesheets', function() {
    gulp.src('css/*.css')
        pipe(makeUrlVer({useDate:true}))
});
```

## Options

assetsDir: specify the public directory for correct MD5 calculation in some specific cases

```js
var makeUrlVer = require('gulp-timestamp-css-url');

gulp.task('stylesheets', function() {
    gulp.src('css/*.css')
        .pipe(makeUrlVer({
            assetsDir: __dirname + '/public'
        }))
});
```

## Example

### before: style.css

```css
.class{background:url(myfile.jpg);}    
```

### after: style.css

```css
.class{background:url(myfile.jpg?v=2017080993403);}

```


