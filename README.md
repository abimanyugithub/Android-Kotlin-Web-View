# Webview Kotlin

**MainActivity.kt**
```
package com.example.andon_fln
import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
*import android.webkit.WebView
*import android.webkit.WebViewClient

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        *title = "KotlinApp"
        *val webView = findViewById<WebView>(R.id.webView)
        *webView.webViewClient = WebViewClient()
        *webView.loadUrl("http://tes.com/andon") // ganti link nya
        *val webSettings = webView.settings
        *webSettings.javaScriptEnabled = true
        *webSettings.setDefaultFontSize(6);
    }
}
```
**AndroidManifest.xml**
```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">
    *<uses-permission android:name="android.permission.INTERNET" />

    <application
        *android:usesCleartextTraffic="true"
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.Andon_fln"
        tools:targetApi="31">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
```
    </application>

</manifest>
