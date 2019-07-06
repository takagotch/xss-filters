### xss-filters
---
https://github.com/yahoo/xss-filters

```
npm install xss-filters --save

npm test
npm run-script build
npm run-script docs
```

```js
var express = require('express');
var app = express();
var xssFilters = require('xss-filters');

app.get('/', function(req, res){
  var firstname = req.query.firstname;
  res.send('<h1> Hello, ' + xssFilters.inHTMLData(filename) + '!</h1>');
});
app.list(3000);
```

```html
<!doctype html>
<script src="dist/xss-filters.min.js"></script>
<script>
  var firstname = "...";
  document.write('<h1> Hello, ' + xssFilters.inHTMLData(firstname) + '!</h1>')
</script>

<input id="strJS" value="{{inDoubleQuotedAttr data}}">
```
