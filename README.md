phonegapbuild-receivve-send-intents
===================================

PhoneGap Build Plugin to enable app to receive SEND intents

This plugin adds the following lines to the AndroidManifest.xml file so that the app gets registered to respond to "SEND" intents from other apps.

    <intent-filter>
        <action android:name="android.intent.action.SEND" />
        <category android:name="android.intent.category.DEFAULT" />
        <data android:mimeType="text/plain" />
    </intent-filter>

In order to listen for the intent action in your app you will need to use the WebIntent plugin (https://build.phonegap.com/plugins/363) and process the intent with the following JavaScript:

    window.plugins.webintent.getExtra(WebIntent.EXTRA_TEXT, 
        function(url) {
            // url is the value of EXTRA_TEXT
        }, function() {
            // There was no extra supplied.
        }
    );
