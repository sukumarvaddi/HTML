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

`<link>` tag has features to improve the performance. Look at the following example with `rel` attribute value set to `preload`.

```html
<link rel="preload" href="your_favorite_font.woff" as="font" type="font/woff2" />
```

Here the `preload` value for `rel` attribute lets the author of the document declare fetch requests. This means that the specified resource will be needed very soon. This is a directive to the browser to start loading this resource early in the page life cycle, even before the page rendering starts. As a result the resource is available earlier and is less likely to block the page rendering. This improves the performance of the page.
<br/>
<br/>
Another alternative for performance improvement is setting the `rel` attribute value to `prefetch` as shown below

```html
<link rel="prefetch" href="someImage.png" />
```

Here the `prefetch` value for `rel` attribute makes the browser utilize its idle time to download the specified resource which the user might visit the page in future where that resource is being utilized.

<br/><br/>

A link element can be used with in `body` though it is necessarily not a good idea. A link element can go in the `<body>` tag only if the the link type is **body-ok**. style sheets are **body-ok**. But **do not** use `<link>` with in `<body>` tag
<br/><br/>
Different link types (when `rel` attribute is set to different values) are explained [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types)
<br/><br/>
The following are different link types and my understanding of what they mean .

1.  [alternate](https://developer.mozilla.org/en-US/docs/Web/CSS/Alternative_style_sheets): This is used to provide alternate style sheets for a web page. On firefox browser you can switch to these style sheets from `view` menu's `Page style` option. I could not figure out how to switch to different style on chrome browser.
2.  author: This `rel` value defines a hyper link to the page about the author of this page or providing means to contact the author.
3.  [canonical](https://en.wikipedia.org/wiki/Canonical_link_element): When this value is specified, it prevents duplicate content issues in search engine Optimization
4.  dns-prefetch: Hints the browser that a specified resource in `href` attribute is needed and carry out DNS lookup and handshaking before user access that link.
5.  help: This leads to a resource which gives further help about the current page.
6.  icon: Navigate to the top of this write up to understand this.
7.  license: specifies a hyperlink to the document describing the licensing information.
8.  manifest: This indicates that the linked file is a [web application manifest](https://developer.mozilla.org/en-US/docs/Web/Manifest)
9.  modulepreload: Directs the browser to load module scripts with high priority.
10. next :This indicates that the link will lead to the next resource with in the sequence where the current page is in.
11. more than humans. Read this [article](https://ahrefs.com/blog/nofollow-links/) for better understanding.
12. pingback: I did not understand this properly.
13. prefetch: Explained above.
14. preload: Explained above.
15. prev: Opposite of `next` which is explained at list item `10`
16. search: I did not understand this properly.
17. shorlink: I did not understand this properly.
18. stylesheets: Explained above.

The comprehensive list of `link` tag attributes and their respective values are explained on [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link) on mdn.
