# intercept_android_7.0-

Configuring Burp Suite With Android Nougat

Android changed the default behavior of trusting user installed certificates. It’s no longer possible to just install the Burp CA from the sdcard to start intercepting app traffic. Unless otherwise specified, apps will now only trust system level CAs. The failure happens “invisibly” and is responsible for all the alerts I saw in Burp Suite.

There’s two ways to bypass this, and I’ll walk through them both.

Install the Burp CA as a system-level CA on the device. My recommendation for the easiest solution, but does require a rooted device. Also added benefit of not having to set a lockscreen PIN :)
Modify the manifest and repackage the app. Slightly more work, but doesn’t require root privileges.
Note: I did all this with Burp Suite Pro on my Windows 10 machine and am using an Android 7.1 (API25) Genymotion VM, but the steps should be applicable to any setup.

FOLLOW THIS LINK FOR INDETAILED OVERVIEW:

https://blog.ropnop.com/configuring-burp-suite-with-android-nougat/
