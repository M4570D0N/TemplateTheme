CM-11.0 sample theme template.
==============================

You will need the [Android SDK](http://developer.android.com/sdk/index.html) (API level 19), [Ant](http://ant.apache.org/), and optionally [pngcrush](http://pmt.sourceforge.net/pngcrush/)

Making a theme assumes some previous knowledge of how Android resources
work. This template has a number of examples for various scenarios
of resource overriding

A prebuilt `aapt` is included and used from `build.xml`. If you're the
paranoid kind, build your own using the CM-11.0 source tree. Standard
aapt will _NOT_ work. Additionally, this aapt has been modified from the CM-11.0 source
tree to allow Upper case letters in xml file names for theming certain apps.

The name of the theme must be wherever you find `TemplateTheme` in here.
(manifest, strings, themes, build.xml)

Edit the path to your copy of the android SDK to  `local.properties`

`my.properties` is used to release and sign the packages. It needs 
4 config items:

    key.store=/path/to/your.keystore
    key.alias=appkey
    key.store.password=your-keystore-password
    key.alias.password=

Build Commands
-----------

Build with `ant release`, test with `ant debug`

DO NOT DISTRIBUTE PACKAGES BUILT WITH `ant debug`. The Google Play 
Store doesn't allow them, and you'll be in trouble if you ever
want to put them there.
