# twitterAPI4js
Twitter API Library written in JavaScript

## how to use

1 import these libraries in your html.
  + jquery
  + oauth.js,sha1.js:adress is in following snipet.
  + this library files

2 initialize all the ribraries.

3 call the function of API you want.
  + argument 1: callback function
  + argument 2: JSONs of api parameter.
    + api parameters meet the REST APIs parameters JSON.for example is below:
    + [user_timeline](https://dev.twitter.com/rest/reference/get/statuses/user_timeline)

```html:how2use.html
	<head>
		<script src="path_to_jquery/jquery.js"></script>
		<script src="http://oauth.googlecode.com/svn/code/javascript/oauth.js"></script>
		<script src="http://oauth.googlecode.com/svn/code/javascript/sha1.js"></script>
		<script src="js/TwitterAPI4JS.js"></script>
	</head>
  <body>
		<script>
			var Twitter4JS = new Twitter4JS();
		</script>
		
		<button type="button" onclick="Twitter4JS.statuses_user_timeline('html', {screen_name:'amagasa'});">amagasa</button>
```
