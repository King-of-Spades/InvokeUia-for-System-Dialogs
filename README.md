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
