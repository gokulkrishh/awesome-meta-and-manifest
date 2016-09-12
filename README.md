# Awesome Meta Tag & Manifest

> A collection of meta tags and manifest.json properties available for building progressive web applications.

### Browsers

#### Desktop

 - Google Chrome
 - Mozilla Firefox
 - Opera
 - Edge
 - Safari

#### Mobile

 - Google Chrome
 - Firefox
 - Opera
 - Safari

### Meta Tags

```html
<!-- Main Meta Tags -->
<meta charset="utf-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no">
<meta name="description" content="Description">
<meta name="keywords" content="Keywords">
<title>Page Title</title>


<!-- Android  -->
<meta name="theme-color" content="red">
<meta name="mobile-web-app-capable" content="yes">


<!-- iOS -->
<meta name="apple-mobile-web-app-title" content="Application Title">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="default">


<!-- Windows  -->
<meta name="msapplication-navbutton-color" content="red">
<meta name="msapplication-TileColor" content="red">
<meta name="msapplication-TileImage" content="ms-icon-144x144.png">
<meta name="msapplication-config" content="browserconfig.xml">

<!-- Pinned Sites  -->
<meta name="application-name" content="Application Name">
<meta name="msapplication-tooltip" content="Tooltip Text">
<meta name="msapplication-starturl" content="/">

<!-- Tap highlighting  -->
<meta name="msapplication-tap-highlight" content="no">


<!-- UC Mobile Browser  -->
<meta name="full-screen" content="yes">
<meta name="browsermode" content="application">

<!-- Disable night mode for this page  -->
<meta name="nightmode" content="disable">

<!-- Layout mode -->
<meta name="layoutmode" content="fitscreen">

<!-- Force show image even in text only mode  -->
<meta name="imagemode" content="force">

<!-- Orientation  -->
<meta name="screen-orientation" content="portrait">
```

### Link Tags
```html
<!-- Main Link Tags  -->
<link href="favicon-16.png" rel="icon" type="image/png" sizes="16x16">
<link href="favicon-32.png" rel="icon" type="image/png" sizes="32x32">
<link href="favicon-48.png" rel="icon" type="image/png" sizes="48x48">

<!-- iOS  -->
<link href="touch-icon-iphone.png" rel="apple-touch-icon">
<link href="touch-icon-ipad.png" rel="apple-touch-icon" sizes="76x76">
<link href="touch-icon-iphone-retina.png" rel="apple-touch-icon" sizes="120x120">
<link href="touch-icon-ipad-retina.png" rel="apple-touch-icon" sizes="152x152">

<!-- Startup Image  -->
<link href="touch-icon-start-up-320x480.png" rel="apple-touch-startup-image">

<!-- Pinned Tab  -->
<link href="path/to/icon.svg" rel="mask-icon" size="any" color="red">

<!-- Android  -->
<link href="icon-192x192.png" rel="icon" sizes="192x192">
<link href="icon-128x128.png" rel="icon" sizes="128x128">

<link href="favicon.icon" rel="shortcut icon" type="image/x-icon">

<!-- Manifest.json  -->
<link href="/manifest.json" rel="manifest">
```


### Manifest
```json
{
  "name": "app name",
  "short_name": "short name",
  "icons": [{
    "src": "images/icons/icon.png",
    "sizes": "192x192",
    "type": "image/png"
  }],
  "gcm_sender_id": "123456",
  "gcm_user_visible_only": true,
  "start_url": "/?utm_source=homescreen",
  "permissions": [
    "gcm"
  ],
  "orientation": "",
  "display": "standalone",
  "theme_color": "#ffffff",
  "background_color": "#ffffff"
}
```

### Few issue and fixes

#### Android

-

#### iOS

- In safari mobile browser, add to home screen will add black background for icon if its in PNG format. Make it as JPG to work.

#### Windows

-

#### UC Browser


### Tools

- [Manifest Validator](https://manifest-validator.appspot.com)

- [Add To Home Ccon Generator](https://romannurik.github.io/AndroidAssetStudio/index.html)

- [Icon Size Generator](http://realfavicongenerator.net/)

### References

- [Apple Developer Site](https://developer.apple.com/library/ios/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)

- [Android](https://developer.chrome.com/multidevice/android/installtohomescreen)

- [UC Browser](http://www.uc.cn/download/UCBrowser_U3_API.doc)

- [Microsoft Internet Explorer](https://github.com/joshbuchea/HEAD#microsoft-internet-explorer )

- [HEAD](https://github.com/joshbuchea/HEAD)


#### MIT Licenced
