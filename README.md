# AndroidMiscUtils
Android utils for context and thread.

### Add Gradle Dependencies

```groovy
dependencies {
    compile 'com.nillith:miscutils:0.2.2'
}
```

### How to use
###1 Init
Init MiscUtils in you Application class.
```java
public class App extends Application {
    @Override
    public void onCreate() {
        super.onCreate();
        MiscUtils.init(getApplicationContext()); // Init MiscUtils
    }
}
```

Add the above class to AndroidManifest.xml
```xml
    <application
        android:name=".App"
```

###2 Supported Operations
####2.1 Static Fields
```java
     MiscUtils.MAIN_HANDLER //Handler for main thread
     MiscUtils.SCHEDULED_EXECUTOR
```

####2.2 Static Methods
```java
     void MiscUtils.init(Context applicationContext)
     MiscUtils.getApplicationContext()
     MiscUtils.isUiThread()
     MiscUtils.isUiThread(Thread thread)
     MiscUtils.runOnUiThread(Runnable runnable)
     MiscUtils.runOnUiThread(Runnable runnable, long delayMillis)
     MiscUtils.runSeriallyOnBackgroundThread(Runnable runnable)
     MiscUtils.runOnBackgroundThread(Runnable runnable)
     MiscUtils.runOnBackgroundThread(Runnable runnable, long delayMillis)
     MiscUtils.showToast(CharSequence message)
     MiscUtils.showToast(@StringRes int resId)
     MiscUtils.showToast(CharSequence message, int duration)
     MiscUtils.showToast(@StringRes int resId, int duration)
     MiscUtils.inflateLayout(View view, @LayoutRes int resId)
     MiscUtils.inflateLayout(Activity activity, @LayoutRes int resId)
     MiscUtils.inflateLayout(Window window, @LayoutRes int resId)
     MiscUtils.inflateLayout(Dialog dialog, @LayoutRes int resId)
     MiscUtils.inflateLayout(@LayoutRes int resId)
     MiscUtils.inflateLayout(Context context, @LayoutRes int resId)
     MiscUtils.attachLayout(ViewGroup viewGroup, @LayoutRes int resId)
```

####2.3 Class
```java
     SimplePagerAdapter
     MatchParentDialog
```


## License

Nillith, 2016. Licensed under an [Apache-2](LICENSE.txt) license.