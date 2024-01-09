# Header Design

You can customize the appeal of the header by easily changing its size, color, adding a border, or modifying its content colors.

## How to change Header Design?

Press the "paint bucket" icon to access the Header Settings page. 

![image](https://github.com/vveretko/vveretko/assets/72790181/466d32ca-3872-4753-bab5-5aec17f2a50c)

## Header settings:

**Theme** - Define how the header will appear in different app themes.

**Background color** - Choose any color you want and the header background will change accordingly.

**Content design** - Select from Dark or Light content colors to ensure the header content looks good on your custom background.

**Datastream (optional)** - For setProperty.

**Border -** You can apply a bottom stroke or a shadow to the header body to separate it from other content.

### **Change Header Properties**

You can change certain properties of the Header from your hardware. For that, use this command:

`Blynk.setProperty(vPin, "headerProperty", "propertyValue");`

Where:

`vPin` is: virtual pin number the widget is assigned to

`headerProperty`: property you want to change

`propertyValue`: value of the property you want to change

Don't put **`Blynk.setProperty()`**into the **`void loop()`** as it can cause a flood of messages and your hardware will be disconnected. Send such updates only when necessary, or use timers.

### **Properties you can change**

You can change the *color* and *contentDesign* properties from your hardware, or via an [HTTP API](notion://www.notion.so/en/blynk.cloud). The URL must be encoded, so spaces in labels must be replaced with %20, and color hexadecimal values in the HTTP API URL must include the hash # character urlencoded as %23.

#### Set color
//#D3435C - Blynk RED
Blynk.setProperty(V1, "color", "Air temperature");
#### Set Color
//#D3435C - Blynk RED 
Blynk.setProperty(V1, "color", "#D3435C");

## Resizing

In the default state, the header size depends on its content. However, you can manually change the size by dragging the handle at the bottom of it.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/20341bdb-5e1a-4881-895e-6e08b23ae969/35769529-59ce-416b-a9fb-83eec09c38e3/Untitled.png)

Presets - maybe when the flow is finilized???
