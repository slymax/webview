This is a template project for Android Studio that allows you to create an android webview application in minutes. You can use it to create a simple app for your website or as a starting point for your HTML5 based android app.

### Getting started

1. [Install Android Studio](http://developer.android.com/sdk/index.html), make sure that the [Android SDK Tools](http://developer.android.com/sdk/index.html#Other) are properly installed and install the [appropriate packages](http://developer.android.com/sdk/installing/adding-packages.html) for the platforms you want to target.

2. [Download](https://github.com/slymax/webview/archive/master.zip) or clone this repository and import it into Android Studio.

### Using a remote source

If you want to create an app that displays the contents of a remote website

1. uncomment **line 31** in `MainActivity.java` and change `http://example.com` to match your remote source

	```
	mWebView.loadUrl("http://example.com");
	```

2. uncomment **line 34**

	```
	mWebView.setWebViewClient(new MyAppWebViewClient());
	```

3. open the `MyAppWebViewClient.java` file and replace `example.com` in **line 12** with your custom url

	```
	if (Uri.parse(url).getHost().endsWith("example.com")) {
	```

### Using a local source

If you want to create a local HTML5 android app

1. uncomment **line 37** in `MainActivity.java`

	```
	mWebView.loadUrl("file:///android_asset/www/index.html");
	```

2. replace the boilerplate website in `src/main/assets/www/` with your own HTML, CSS and JavaScript files