# &lt;link&gt; tag

`<link>` tag specifies relationship between the current document and external resources. This is a multipurpose tag.

It is used to provide external links to CSS as shown below. The `rel` attribute of this tag stands for 'relationship'

```html
<link href="styles.css" rel="stylesheet" />
```

This tag is not limited to connecting the current document with external style sheets. It is also used to establish site icons such as favicons, home screen icons for web applications on mobile devices.
To specify an favicon you can use link tag as follows

```html
<link rel="icon" href="favicon.ico" />
```

To specify an icon for a home screen on mobile devices, you can use link tag as follows

```html
<link rel="apple-touch-icon" href="/custom_icon.png" />
```

[Click here](https://developer.apple.com/library/archive/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html) for a detailed explanation on how to add home screen icons on IOS devices.

`<link>` tag can be provided with `media` attribute which takes either a media type such as `print` or media query as its value. By using `<link>` tag in this manner, you can load the resource when the condition is true. This trick is used in optimizing the performance of the web application.

```html
<link href="style.css" rel="stylesheet" media="print" />
```

The above stylesheet is not loaded when the browser load the document for viewing. This is loaded and applied when you try to print the document.

Here is an example of `<link>` used with media query .

```html
<link href="style.css" rel="stylesheet" media="screen and (max-width: 500px)" />
```

This style sheet is loaded when the value specified for `media` attribute is evaluated to true.
