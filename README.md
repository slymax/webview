This is a template project for Android Studio that allows you to create an android webview application in minutes. You can use it to create a simple app for your website or as a starting point for your HTML5 based android app.

### Getting started

[Download](https://github.com/slymax/webview/archive/master.zip) or clone this repository and import it into Android Studio.

### Using a remote source

If you want to create an app that displays the content of a remote website

1. uncomment lines **30** and **31** in `MainActivity.java` and replace `http://example.com` with your remote source

	```java
	mWebView.loadUrl("http://example.com");
	mWebView.setWebViewClient(new MyWebViewClient());
	```

2. open the `MyWebViewClient.java` file and replace `example.com` on line **14** with your custom hostname

	```java
	if (Objects.requireNonNull(Uri.parse(url).getHost()).endsWith("example.com")) {
	```

### Using a local source

If you want to create a local HTML5 android app

1. uncomment line **34** in `MainActivity.java`

	```java
	mWebView.loadUrl("file:///android_asset/index.html");
	```

2. put all your files (including your `index.html`) in the `assets` directory
