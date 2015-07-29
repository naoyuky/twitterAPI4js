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
	</body>
```

## For Developing
I made some examples of callback function.
+ cbname:print the whole JSON data to console directry.
+ html:print only screen_name,text,name to #test1.
+ htmljson:print the whole JSON data to #test1.

## NOTE
+ some important key is opened if you use this library for the frontend application. Please use this carefully, or only use it for private application.
+ I checked the working of only these APIs. Some API adress might be wrong. Please correct and send me a pull request.
	+ statuses_user_timeline
	+ statuses_mentions_timeline
	+ statuses_home_timeline
+ GETメソッドはひとつも動作成功していないので、対応のために大規模変更が加わる可能性があります。

# Japanese
は～英語疲れた。母国語のほうがラクなのは当たり前なんですけどね。
私のいい加減な英語を再翻訳していただくくらいなら、直接日本語で説明を。

## 使い方
基本的に使い方は上の説明コードを見ていただければだいたい分かるかと思いますが……
1. Twitterのアプリケーション登録をする
	1. consumerKey,consumerSecret,accessToken,tokenSecretを取得する
	1. consumerKey: "", consumerSecret: "", accessToken: "", tokenSecret: "" のセミコロンの間にそれぞれ入力してください。

1. 必要なもの
	+ これらをインポートしてください。
		+ jquery
		+ googlecode[1](http://oauth.googlecode.com/svn/code/javascript/oauth.js),[2](http://oauth.googlecode.com/svn/code/javascript/sha1.js)で公開されているoauthのjavascriptライブラリ
		+ TwitterAPI4js.js

1. オブジェクト全体を初期化してください

1. それぞれのAPIに対応した関数が用意されているので、関数を呼び出してください。
	+ 第一引数はコールバック関数(必須)
	+ 第二引数はTwitterAPIに投げるパラメータJSON(APIによっては必須。dev.twitter.comの各APIを参照して、必須項目が入ったJSONを渡してください。)
		+ JSONはTwitterAPIにそのまま投げてしまうので、要素名などの例はdev.twitter.comを見て頂いてそれに対応させてください。[例→user_timeline](https://dev.twitter.com/rest/reference/get/statuses/user_timeline)
		+ JSON手書きは拡張性低いよ〜めんどくさいよ〜ってことであれば、更に拡張して代入しやすい関数を実装したほうが良さそうですね……

## 開発のために
コールバック関数の例として、挙動確認のために簡単な関数を用意しました。他にも色々関数用意していただけると。そして教えてください。
+ cbname:コンソールにJSONをそのまま吐き出します。
+ html:スクリーンネーム、ツイート内容、名前だけをHTMLの#test1に出力します。
+ htmljson:HTMLの#test1にJSONをそのまま吐き出します。

## 注意点
+ consumerKeyなどのキーが他者に丸見えになっているので、自分で使う簡単なアプリケーションの作成や、プログラミングの練習用に利用することは可能ですが、公開するアプリケーションのフロントエンドにそのまま渡さないよう注意してください。キーが漏れるとあなたのアプリとユーザーを悪用できちゃいます。
+ 2015年7月29日現在、動作確認しているAPIは以下のもののみです(全体を拡張しやすくすることを優先したため)。APIのアドレスが間違っていたり、仕様変更によって使えなくなったりする可能性もあります。その場合は各自で訂正していただいて、pull reqください。
	+ statuses_user_timeline
	+ statuses_mentions_timeline
	+ statuses_home_timeline
+ GETメソッドはひとつも動作成功していないので、対応のために大規模変更が加わる可能性があります。
