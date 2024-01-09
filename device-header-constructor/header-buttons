# Header buttons

You can add up to 2 header buttons and assign a Standalone Page to each of them.

To add a header button, simply click the “plus” icon at the top of the header, and its settings will open.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/6c9265cb-1448-4037-8b98-27e41bda66ad/Untitled.png)

## Header button settings:

**Datastream (optional)** - For setProperty.

**Page** - Select a page to open when pressing this button on the Device Dashboard. Only Standalone Pages are supported.

**Icon** - Define how this button will appear to the user.

**Appearance Animation** - The page can slide in from the bottom or from the right.

### **Change Header Button Properties**

You can change *isHidden* of the Header from your hardware. For that, use this command:

`Blynk.setProperty(vPin, "isHidden", "propertyValue");`

Where:

`vPin` is: virtual pin number the widget is assigned to

`isHidden`: property that controls the button visibility

`propertyValue`: value of the property you want to change. *true* and *false* values are available.

Don't put **`Blynk.setProperty()`**into the **`void loop()`** as it can cause a flood of messages and your hardware will be disconnected. Send such updates only when necessary, or use timers.

### **Change widget properties via HTTPs API**

https://{server_address}
/external/api/update/property?token={your 32 char token}&pin={your vPin}&{property}={value}
Updates the Datastream Property and all assigned Widgets
