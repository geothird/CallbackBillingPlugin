Callback In App Billing Plugin
==============================

This plugin is based on the sample in app billing app Dugeons provided by Google: http://code.google.com/p/marketbilling/


Installation
------------
-   From the main_java.txt file in this repo:

    Cut and paste the "Billing -imports- Additions" into the the app's main java file imports section.
    Cut and paste the "Billing -main Activity- Additions" into the main activity class.
    After "super.onCreate(savedInstanceState);", cut and paste the "Billing -onCreate- Additions" into the main activity onCreate function.
    

-   Create src/com/phonegap/plugin/billing/plugin and add the following files from the repo:

    Base64.java
    Base64DecoderException.java
    BillingReceiver.java
    BillingService.java
    CallbackBillingPlugin.java
    Consts.java
    PurchaseDatabase.java
    PurchaseObserver.java
    ResponseHandler.java
    Security.java
     
-   Fix errors in your main java file and CallbackBillingPlugin.java by:

    Replacing all references to "CallbackBillingActivity" with the your main activity.
    In CallbackBillingPlugin.java, change "import com.phonegap.plugin.billing.CallbackBillingActivity;" to imoprt your main activity.

-   Create src/com/android/vending/billing and add IMarketBillingService.aidl from the repo.

-   Add your market public key in Security.java:

    String base64EncodedPublicKey = "your public key here";
    

-   Add plugin_billing.js to assets/www from the repo and include it from your index.html:

    <script type="text/javascript" src="plugin_billing.js"></script>
    

-   Add the following to res/xml/config.xml (or plugins.xml):

    <plugin name="CallbackBillingPlugin" value="com.phonegap.plugin.billing.plugin.CallbackBillingPlugin"/>


Usage
-----
-   You can only test the plugin on a physical device.

-   More usage information will be added soon.  For now see the sample app or js file.


Change Log
----------
11/05/2012: Updated this README to include installation instructions.
            Removed commented code from sample project.
            Added stand-alone plugin files.
            

11/04/2012: Updated for Cordova 2.0.0 (used geothird 1.9.0 base and added macdonst's js plugin file).
            Reorganized main java file in prep for stand-alone plugin.