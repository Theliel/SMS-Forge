# SMS Forge: The Swiss Army Knife of SMS

![SMSForge](https://github.com/user-attachments/assets/a72b7290-a991-48ab-bab8-23e8075b5031)

First, we need to talk about what SMS Forge is (and isn't).

SMS Forge isn't a conventional SMS application; it wasn't designed as an SMS manager, nor to be used as a replacement for system SMS applications, nor even to receive SMS (with a few exceptions). SMS Forge is a project I've had in mind since the pre-Android era, strongly inspired by the old management software "floAt's Mobile Agent," where I first learned how complex and rich SMS really was, and how extremely limited current SMS applications are. Today, IM has largely replaced the old SMS system, but for many enthusiasts, like myself, we can say that better late than never.

Throughout Android's history, we've been fortunate enough to see a few developers explore the feasibility of creating "advanced" SMS applications, most notably the well-known Class 0 SMS (also known as Flash SMS). Unfortunately, while Google's original APIs allowed developers to create applications for this, they were removed long time ago. This is the case with older apps like FlashSMS, which could work on a very limited number of devices. Somewhat later, and thanks primarily to rooted devices and the EdXposed framework, apps like HushSMS or GAT-App emerged, using EdXposed to intercept internal Android calls that were still available. Unfortunately, again, this was limited not only to having a rooted device, but also to using EdXposed (sometimes a headache for those who use banking apps) and only for older Android versions.

This is where SMS Forge was born, thanks, as I say, to the vision that the FMA developers had many years ago. The goal of SMS Forge is to have a simple tool on our devices capable of sending a wide range of different SMS messages, taking advantage of the richness of GSM standards, and supporting up to day Android devices. All of this breaks down some of the barriers that existed years ago, like limiting its use to a "few" devices. This doesn't mean that SMS Forge can be used on any device (I wish it were). The bad news is that SMS Forge will still require a rooted device for now. The good news, on the other hand, is that it won't require EdXposed or any Magisk Module, only root permissions. Of course, it's compatible with modern versions of Android (tested up to A15). It was initially designed for Android 9 and later, although this shouldn't be a problem if there's significant interest in using older Android versions.

As will be explained later in the FAQ, each manufacturer/device may have different peculiarities that may cause SMS Forge to have some limitations, or be completely incompatible. The idea in the future is to explore different ways to try to maximize compatibility, possibly even including some devices without root. Similarly, when we send an SMS from SMS Forge, we can never guarantee or ensure how the receiving device will interpret it. For example, a Class 0 SMS on a Samsung/Xiaomi device with an A15 will be displayed directly on the screen, allowing us to see both the sender and the option to save it; on iOS, neither the name nor the option appears. Other types of SMS may be directly discarded by the device or have no effect.

The project is far from being finalized; the idea is to continue implementing features, greater control over sending options, and seeking viable alternatives to some existing limitations. Initially, the project will likely be licensed commercially and published on Google Play (there's always the option to ban it). Depending on various factors, I may eventually change my mind and publish it completely openly.


# Implemented Features and To-Do

Already Implemented:

+ All SMS Class: 0(Flash)/1(ME)/2(SIM)/3(Reserved)
+ Replace SMS
+ Auto-Delete SMS
+ Message Waiting Indicator: DCS or UDH
+ Silent/Ping SMS: Type 0 or MWI
+ Status Report: See FAQ, with some limitations at the moment
+ National/International Number Support
+ Automatic charset detection (GSM7/160ch. UCS2/70ch)
+ Automatic Light/Dark Theme. 
+ Mediatek support


To-Do

- Interface redesign
- Translation into other languages
- SMS RAW
- SMS WAP
- SMS for MMS Notification
- Path-Reply
- Valid-Period, Reject Duplicates, Message Reference, and SMSC
- Perhaps a permanent way to work around the limitations of current status reports
- SMS Compression
- Long SMS (Concatenation)
- More to come...
- Lite/Test SMS Forge version


# Limitations

As explained, there are some limitations that may prevent partial or complete use of SMS Forge. Some of these are easily remedied and are due to the inability to individually check the compatibility/behavior between the different devices currently on the market, different SoCs, and Basebands. I will soon publish a simple APK here so that anyone who wants to can install/check on their device whether it is potentially compatible or not, and if not, they can attach a report to see if it can be implemented.

Currently, it has been tested on several devices with Qualcomm SoCs of different generations, and some MediaTek devices. MediaTek devices are a bit more complex, and the logic still needs to be fully implemented. Even so, minor adjustments may be necessary to cover more devices.
