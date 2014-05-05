phonegapbuild-receivve-send-intents
===================================

PhoneGap Build Plugin to enable app to receive SEND intents

This plugin adds the following lines to the AndroidManifest.xml file so that the app gets registered to respond to "SEND" intents from other apps.

    <intent-filter>
        <action android:name="android.intent.action.SEND" />
        <category android:name="android.intent.category.DEFAULT" />
        <data android:mimeType="text/plain" />
    </intent-filter>
