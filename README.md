Note: Xcode 8 / iOS 10 removed UIAutomation; so the approach will not work on these versions. 
More information on how iOS 10 changes affect UITest is available here: https://developer.xamarin.com/guides/testcloud/uitest/working-with/ios-10/

InvokeUia for System Dialogs 
============================
This sample uses the "Push Notification" sample from https://github.com/xamarin/monotouch-samples/tree/master/Notifications, but adds a UITest to dismiss the system dialog:

To use this, substitute *OK* for the label of the button you wish to press in the dialog.

```cs
[Test]
public void AppLaunches ()
{
	app.Screenshot ("First screen.");
	app.InvokeUia ("uia.query('[:view {:marked \"OK\"}]')"); 
	app.InvokeUia ("uia.tapMark(\"OK\")"); 
}
```
