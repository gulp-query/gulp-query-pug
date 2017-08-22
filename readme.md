## gulp-query-pug
PUG plugin for [gulp-query](https://github.com/gulp-query/gulp-query)

Uses [pug](https://www.npmjs.com/package/pug)

This plugin provides high performance template engine.

```
npm install gulp-query gulp-query-pug
```

### Example
Paste the code into your `gulpfile.js` and configure it
```javascript
let build = require('gulp-query')
  , pug = require('gulp-query-pug')
;
cocktail(function (query) {
    query.plugins([pug])
      .pug('src/views/*.pug','html/','tpl')

      .pug({
        from: ['src/views/*.pug','src/views/auth/*.pug'],
        to: 'html/',
        name: 'views'
      })
      ;
});
```
And feel the freedom
```
gulp
gulp --production // For production
gulp watch // Watching change
gulp pug // Only for pug
gulp pug:tpl // Only pug:tpl
gulp pug:views watch // Watching change only for pug:views
...
```

### Options
```javascript
.pug({
    name: "task_name", // For gulp pug:task_name 
    from: "views/*.pug", // ['src/views/*.pug','src/views/auth/*.pug']
    to: "html/"
})
```