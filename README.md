This is a template project for Android Studio that allows you to create an android webview application in minutes. You can use it to create a simple app for your website or as a starting point for your HTML5 based android app.

### Getting started

[Download](https://github.com/slymax/webview/archive/master.zip) or clone this repository and import it into Android Studio.

### Using a remote source

If you want to create an app that shows the content of a remote website

1. uncomment line **24** in `MainActivity.java` and replace `https://example.com` with your url

	```java
	mWebView.loadUrl("https://example.com");
	```

2. open the `MyWebViewClient.java` file and replace `example.com` on line **15** with your hostname

	```java
	hostname = "example.com";
	```

### Using a local source

If you want to create a local HTML5 android app

1. uncomment line **27** in `MainActivity.java`

	```java
	mWebView.loadUrl("file:///android_asset/index.html");
	```

2. put all your files (including your `index.html`) in the `assets` directory

### Building your app for Play Store

When you are ready to release your app and have test the app in Studio virtual simulator (In Android Studio, on the menu, click Run > Run app)

1. Change the app name in app > res > values > strings.xml. This name appears on user's desktops once the app is built and deployed. Optionally change the icons as well at res > mipmap > ic_launcher. 
2. Try to build the APK file. This is a raw APK file that you can install into your mobile for testing. In Android studio, Build > Build Bundle APK > Build APK
3. If the APK file gets built, then BEFORE loading the APK file into your mobile, test the APK file at virustotal.com to make sure it isn't flagged. Many APK files across the web have viruses, so this should be good security practice. 
4. Test the APK file again at MetaDefender https://metadefender.opswat.com/
5. Let Google virus scan your file. Copy the APK file to your Google Drive. Within a few minutes, if there is a virus in the file, Google will send you an email. If not, you won't get an email.
6. If all the virus testing passes, then install the APK file into your phone by either emailing the file to yourself, or using a remote FTP connection into your phone. The File Manager app lets you do this. https://play.google.com/store/apps/details?id=com.alphainventor.filemanager
7. Test your app on your phone
8. If it works on your phone, then build the package for uploading to Google Play store
9. Locate the build.gradle (module.app) file on the left hand side in Android Studio
10. Change line 7 so that it does NOT say "example". Replace the word "example" with your custom app name. Ideally your domain name would be here. So for example, if your domain was JohnsApplePies.com, then line 7 for applicationID could be "com.johnsapplepies.app"
11. Generate your APK file again from step 1 to step 6 above and re-run all scans
12. In Android Studio, go to Build menu, and choose "Generate Signed Bundle / APK"
13. Follow VERY CLOSELY the instructions provided here to create a key, password, etc: https://developer.android.com/studio/publish
14. Visit https://play.google.com/console/ to setup your account, upload your release, verify your identity etc
