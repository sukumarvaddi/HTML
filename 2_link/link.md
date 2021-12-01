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

<a href='https://developer.apple.com/library/archive/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html' target="_blank"> Click Here </a>for a detailed explanation on how to add home screen icons on IOS devices.
