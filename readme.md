## gulp-timestamp-css-url

a plugin for gulp.js to add timestamps to images and fonts in CSS files


## Installation

```bash
npm install gulp-timestamp-css-url
```

## Usage

```js
var cssTimeStamp = require('gulp-timestamp-css-url');

gulp.task('stylesheets', function() {
    gulp.src('css/*.css')
        pipe(cssTimeStamp({useDate:true}))
});
```

## Options

assetsDir: specify the public directory for correct MD5 calculation in some specific cases

```js
var cssTimeStamp = require('gulp-timestamp-css-url');

gulp.task('stylesheets', function() {
    gulp.src('css/*.css')
        .pipe(cssTimeStamp({
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


