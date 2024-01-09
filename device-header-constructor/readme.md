# Device header constructor

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/45db1e25-5f32-4ea6-bea5-9f1d6f6dfe7d/Untitled.png)

The header constructor allows you to customize the header of your device according to your preferences. You can add important labels such as Connection Status and Last Reported timestamp, display an image inside the device's header, or assign Standalone Pages to the Header Buttons. You can also experiment with colors to make it more visually appealing.

## Header buttons

You can add up to 2 header buttons and assign a Standalone Page to each of them.

To add a header button, simply click the “plus” icon at the top of the header, and its settings will open.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/6c9265cb-1448-4037-8b98-27e41bda66ad/Untitled.png)

### Header button settings:

**Datastream (optional)** - For setProperty.

**Page** - Select a page to open when pressing this button on the Device Dashboard. Only Standalone Pages are supported.

**Icon** - Define how this button will appear to the user.

**Appearance Animation** - The page can slide in from the bottom or from the right.

#### **Change Header Button Properties**

You can change *isHidden* of the Header from your hardware. For that, use this command:

`Blynk.setProperty(vPin, "isHidden", "propertyValue");`

Where:

`vPin` is: virtual pin number the widget is assigned to

`isHidden`: property that controls the button visibility

`propertyValue`: value of the property you want to change. *true* and *false* values are available.

Don't put **`Blynk.setProperty()`**into the **`void loop()`** as it can cause a flood of messages and your hardware will be disconnected. Send such updates only when necessary, or use timers.

#### **Change widget properties via HTTPs API**

https://{server_address}
/external/api/update/property?token={your 32 char token}&pin={your vPin}&{property}={value}
Updates the Datastream Property and all assigned Widgets


## Header Design

You can customize the appeal of the header by easily changing its size, color, adding a border, or modifying its content colors.

### How to change Header Design?

Press the "bucket" icon to access the Header Settings page. 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/6a6cc2d7-a569-4450-a6d0-5bc28ff81194/Untitled.png)

### Header settings:

**Theme** - Define how the header will appear in different app themes.

B**ackground color** - Choose any color you want and the header background will change accordingly.

**Content design** - Select from Dark or Light content colors to ensure the header content looks good on your custom background.

**Datastream (optional)** - For setProperty.

**Border -** You can apply a bottom stroke or a shadow to the header body to separate it from other content.

#### **Change Header Properties**

You can change certain properties of the Header from your hardware. For that, use this command:

`Blynk.setProperty(vPin, "headerProperty", "propertyValue");`

Where:

`vPin` is: virtual pin number the widget is assigned to

`headerProperty`: property you want to change

`propertyValue`: value of the property you want to change

Don't put **`Blynk.setProperty()`**into the **`void loop()`** as it can cause a flood of messages and your hardware will be disconnected. Send such updates only when necessary, or use timers.

#### **Properties you can change**

You can change the *color* and *contentDesign* properties from your hardware, or via an [HTTP API](notion://www.notion.so/en/blynk.cloud). The URL must be encoded, so spaces in labels must be replaced with %20, and color hexadecimal values in the HTTP API URL must include the hash # character urlencoded as %23.

#### Set color
//#D3435C - Blynk RED
Blynk.setProperty(V1, "color", "Air temperature");
#### Set Color
//#D3435C - Blynk RED 
Blynk.setProperty(V1, "color", "#D3435C");

### Resizing

In the default state, the header size depends on its content. However, you can manually change the size by dragging the handle at the bottom of it.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/35769529-59ce-416b-a9fb-83eec09c38e3/Untitled.png)

Presets - maybe when the flow is finilized???

## Header Widgets

Header widgets enable the display of important information in the device header, such as battery level, the last reported timestamp, datastream value, and more.

### **Adding and Deleting**

To add a header widget, click on the "plus" icon located below the Template name, which will open the Widget Box. Select the desired widget from the available options.

Once the first widget is added, you'll notice two “plus” icons, enabling you to add widgets in different rows for enhanced customization.

To remove a widget, press on it to access its settings, and then tap the “trash” icon positioned at the top right corner. This will promptly delete the selected widget from your configuration.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/89fd1b73-6716-4496-9e49-6ac76e9fd767/Untitled.png)

### Connection Status widget

This widget displays the device’s current status as a text label.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/5ba7781d-5d2e-45b8-913c-c4d9d57f7909/Untitled.png)

#### Settings

**Datastream (optional)** - For setProperty.

#### **Change Widget Properties**

You can change certain properties of the Widget from your hardware. For that, use this command:

`Blynk.setProperty(vPin, "widgetProperty", "propertyValue");`

Where:

`vPin` is: virtual pin number the widget is assigned to

`widgetProperty`: property you want to change

`propertyValue`: value of the property you want to change

Don't put **`Blynk.setProperty()`**into the **`void loop()`** as it can cause a flood of messages and your hardware will be disconnected. Send such updates only when necessary, or use timers.

#### **Properties you can change**

You can change the properties *isDisabled and* *isHidden* of the widget from your hardware, or via an [HTTP API](notion://www.notion.so/en/blynk.cloud). The URL must be encoded, so spaces in labels must be replaced with %20.

### Last Reported widget

This widget shows the timestamp of the last time Blynk received the data from the device.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/04d5601d-bd99-4730-966e-1d8474fcf323/Untitled.png)

#### Settings

**Datastream (optional)** - For setProperty

For example:

`Blynk.setProperty(V3, "isHidden", "true");` - this will hide the widget.

It works only for virtual, enumerable, and location pins, not digital and analog pins.

**Show icon** - To show/hide the “Clock” icon on the left.

**Show label** - To show/hide the “Last reported” text.

#### **Change Widget Properties**

You can change certain properties of the Widget from your hardware. For that, use this command:

`Blynk.setProperty(vPin, "widgetProperty", "propertyValue");`

Where:

`vPin` is: virtual pin number the widget is assigned to

`widgetProperty`: property you want to change

`propertyValue`: value of the property you want to change

Don't put **`Blynk.setProperty()`**into the **`void loop()`** as it can cause a flood of messages and your hardware will be disconnected. Send such updates only when necessary, or use timers.

#### **Properties you can change**

You can change the properties *isDisabled and* *isHidden* of the widget from your hardware, or via an [HTTP API](notion://www.notion.so/en/blynk.cloud). The URL must be encoded, so spaces in labels must be replaced with %20.

### Tabs widget

Adds one or more tabs to the top of the device mobile dashboard in order to expand and organize the user interface space. You can drag widgets between tabs.
Note that plan limits apply here.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/eb55df15-c356-453e-9d6a-a704c5852401/Untitled.png)

#### **Navigating the Tabs Editor:**

To access the Tabs editor, simply tap on the active tab. In the editor, you can rename tabs, alter their order, add new tabs, and swipe left to delete a tab. Note that the last two tabs are permanent and cannot be removed, but you can delete the entire widget by pressing the “Trash” icon located at the top right.

#### **Moving Widgets Between Tabs:**

1. Press and hold the widget you wish to move.
2. Drag it over the tab where you want it to be placed and hold until the tab opens.
3. Release the widget in the desired position to seamlessly move it between tabs.

### Datastream Value widget

Displays the latest datastream / virtual pin value. Units assigned to the datastream are also displayed. Labels may also be optionally added before and after the displayed value.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/e2de0c53-6a7e-4998-822a-4abae68c2239/Untitled.png)

#### Settings

**Datastream** - Select or create a datastream of [data type](notion://www.notion.so/en/blynk.console/templates/datastreams/datastreams-common-settings/data-type) integer, double, enumerable or string.

**Label** - Set custom label before the value. E.g Temperature: `/value/`

#### **Change Widget Properties**

You can change certain properties of the Widget from your hardware. For that, use this command:

`Blynk.setProperty(vPin, "widgetProperty", "propertyValue");`

Where:

`vPin` is: virtual pin number the widget is assigned to

`widgetProperty`: property you want to change

`propertyValue`: value of the property you want to change

Don't put **`Blynk.setProperty()`**into the **`void loop()`** as it can cause a flood of messages and your hardware will be disconnected. Send such updates only when necessary, or use timers.

#### **Properties you can change**

You can change the properties *isDisabled and* *isHidden* of the widget from your hardware, or via an [HTTP API](notion://www.notion.so/en/blynk.cloud). The URL must be encoded, so spaces in labels must be replaced with %20.

### Image widget

Improve your header visually with custom image that can be controlled from hardware.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/633623b6-a872-410c-885d-7a7437e122e9/Untitled.png)

#### Settings

**Theme** - Define how the widget design will appear in different app themes.

**Datastream** - Select or create a datastream of [data type](notion://www.notion.so/en/blynk.console/templates/datastreams/datastreams-common-settings/data-type) integer.

**Handle values out of range as empty -** Toggle ON to display nothing on the widget when the value is outside the expected range. If this setting is turned OFF, the image closest to the current value will be shown.

**Images** - Specify a list of images to display, where the Image ID corresponds to the respective values of the datastream.

**Full width** - Define the width of the image container to ensure optimal presentation.

**Images scaling** - Choose between FIT or FILL options to adjust how the image appears within the container.

#### **Change Widget Properties**

You can change certain properties of the Widget from your hardware. For that, use this command:

`Blynk.setProperty(vPin, "widgetProperty", "propertyValue");`

Where:

`vPin` is: virtual pin number the widget is assigned to

`widgetProperty`: property you want to change

`propertyValue`: value of the property you want to change

Don't put **`Blynk.setProperty()`**into the **`void loop()`** as it can cause a flood of messages and your hardware will be disconnected. Send such updates only when necessary, or use timers.

#### **Properties you can change**

You can change the properties *isDisabled*, *isHidden, url or urls* of the widget from your hardware, or via an [HTTP API](notion://www.notion.so/en/blynk.cloud). The URL must be encoded, so spaces in labels must be replaced with %20.

### Battery level widget

This widget provides a clear visual representation of your battery level, accompanied by a percentage indicator for quick reference.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/2d9366ae-adb0-473b-9e5f-9905beb3a1c3/Untitled.png)

#### Settings

**Datastream** - Select or create a datastream of [data type](notion://www.notion.so/en/blynk.console/templates/datastreams/datastreams-common-settings/data-type) integer or double.

Value should come in 0-100 range.

**Show value** - You can bide the value to see the battery icon only.

#### **Change Widget Properties**

You can change certain properties of the Widget from your hardware. For that, use this command:

`Blynk.setProperty(vPin, "widgetProperty", "propertyValue");`

Where:

`vPin` is: virtual pin number the widget is assigned to

`widgetProperty`: property you want to change

`propertyValue`: value of the property you want to change

Don't put **`Blynk.setProperty()`**into the **`void loop()`** as it can cause a flood of messages and your hardware will be disconnected. Send such updates only when necessary, or use timers.

#### **Properties you can change**

You can change the properties *isDisabled and* *isHidden* of the widget from your hardware, or via an [HTTP API](notion://www.notion.so/en/blynk.cloud). The URL must be encoded, so spaces in labels must be replaced with %20.

### Tags widget

Display a list of tags assigned to the device.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/e7823fa5-c3c8-4bf5-800c-b8e36a74e211/Untitled.png)

#### Settings

**Datastream (optional)** - For setProperty.

#### **Change Widget Properties**

You can change certain properties of the Widget from your hardware. For that, use this command:

`Blynk.setProperty(vPin, "widgetProperty", "propertyValue");`

Where:

`vPin` is: virtual pin number the widget is assigned to

`widgetProperty`: property you want to change

`propertyValue`: value of the property you want to change

Don't put **`Blynk.setProperty()`**into the **`void loop()`** as it can cause a flood of messages and your hardware will be disconnected. Send such updates only when necessary, or use timers.

#### **Properties you can change**

You can change the properties *isDisabled and* *isHidden* of the widget from your hardware, or via an [HTTP API](notion://www.notion.so/en/blynk.cloud). The URL must be encoded, so spaces in labels must be replaced with %20.