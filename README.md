# twitterAPI4js
Twitter API Library written in JavaScript

# English
## how to use

1. regist the twitter application and get the AccessToken, TokenSecret, consumerKey, consumerSecret
	1. edit the Twitter4JS.options.

1. import these libraries in your html.
	+ jquery
	+ oauth.js,sha1.js:adress is in following snipet.
	+ this library files

1. initialize all the ribraries.

1. call the function of API you want.
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

# Japanese
は～英語疲れた。母国語のほうがラクなのは当たり前なんですけどね。
私のいい加減な英語を再翻訳していただくくらいなら、直接日本語で説明を。

## 使い方
基本的に使い方は上の説明コードを見ていただければだいたい分かるかと思いますが……  
1. Twitterのアプリケーション登録をする  
	+ consumerKey: "", consumerSecret: "", accessToken: "", tokenSecret: "" のセミコロンの間にそれぞれ入力してください。

1. 必要なもの
	+ これらをインポートしてください。
		+ jquery
		+ googlecode[1](http://oauth.googlecode.com/svn/code/javascript/oauth.js),[2](http://oauth.googlecode.com/svn/code/javascript/sha1.js)で公開されているoauthのjavascriptライブラリ
		+ TwitterAPI4js.js

1. オブジェクト全体を初期化してください

1. それぞれのAPIに対応した関数が用意されているので、関数を呼び出してください。
	+ 第一引数はコールバック関数
	+ 第二引数はTwitterAPIに投げるパラメータJSON
		JSONはTwitterAPIにそのまま投げてしまうので、要素名などの例はdev.twitter.comを見て頂いてそれに対応させてください。[例→user_timeline](https://dev.twitter.com/rest/reference/get/statuses/user_timeline)
		JSOn手書きは拡張性低いよ〜めんどくさいよ〜ってことであれば、更に拡張して代入しやすい関数を実装したほうが良さそうですね……
