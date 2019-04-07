# Awesome Meta Tags & Manifest Properties [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)


> Awesome collection of meta tags and manifest properties available for building progressive web applications.

## Browsers Support

### Desktop

 - `Google Chrome`
 - `Mozilla Firefox`
 - `Opera`
 - `Edge`
 - `Safari`

### Mobile

 - `Google Chrome`
 - `Firefox`
 - `Opera`
 - `Safari`
 - `Samsung Internet Browser`
 - `UC Browser` (partial support)

### Meta Tags

```html
<!-- Must -->
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
<meta name="nightmode" content="enable/disable">

<!-- Fitscreen  -->
<meta name="viewport" content="uc-fitscreen=yes"/>

<!-- Layout mode -->
<meta name="layoutmode" content="fitscreen/standard">

<!-- imagemode - show image even in text only mode  -->
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

<!-- Others -->
<link href="favicon.icon" rel="shortcut icon" type="image/x-icon">

<!-- UC Browser  -->
<link href="images/icon-52x52.png" rel="apple-touch-icon-precomposed" sizes="57x57">
<link href="images/icon-72x72.png" rel="apple-touch-icon" sizes="72x72">

<!-- Manifest.json  -->
<link href="/manifest.json" rel="manifest">
```

### Manifest
```json
{
  "name": "app name",
  "short_name": "short name",
  "icons": [{
    "src": "images/icons/icon-48x48.png",
    "sizes": "48x48",
    "type": "image/png"
  },
  {
    "src": "images/icons/icon-72x72.png",
    "sizes": "72x72",
    "type": "image/png"
  },
  {
    "src": "images/icons/icon-96x96.png",
    "sizes": "96x96",
    "type": "image/png"
  },
  {
    "src": "images/icons/icon-144x144.png",
    "sizes": "144x144",
    "type": "image/png"
  },
  {
    "src": "images/icons/icon-168x168.png",
    "sizes": "168x168",
    "type": "image/png"
  },
  {
    "src": "images/icons/icon-192x192.png",
    "sizes": "192x192",
    "type": "image/png"
  },
  {
    "src": "images/icons/icon-256x256.png",
    "sizes": "256x256",
    "type": "image/png"
  },
  {
    "src": "images/icons/icon-512x512.png",
    "sizes": "512x512",
    "type": "image/png"
  }],
  "gcm_sender_id": "",
  "gcm_user_visible_only": true,
  "start_url": "/?utm_source=homescreen",
  "permissions": [
    "gcm"
  ],
  "scope": "",
  "orientation": "portrait",
  "display": "standalone",
  "theme_color": "#ffffff",
  "background_color": "#ffffff"
}
```

### Some issues in browsers & its fixes

#### `Android`

- Icons for manifest.json, doesn't need to have many icons. Adding ```192px``` size icon will scale perfectly for most of the devices.
- ```gcm_user_visible_only``` key removed in [Chrome 45](https://www.chromestatus.com/feature/5778950739460096) favor of the specified solution: [```userVisibleOnly```](https://developer.mozilla.org/en-US/docs/Web/API/PushManager/subscribe). 

#### `iOS`

- In safari mobile browser, add to home screen will add black background for icon if its in PNG format. Make it as JPG to work.
- Safari doesn't support manifest.json for add to home screen yet.

#### `UC Browser`

- Meta tag ```browsermode``` is not working.
- Link tag ```icon``` for home screen is not working.

### Tools

- [Manifest Validator](https://manifest-validator.appspot.com)
- [Add To Home Icon Generator](https://romannurik.github.io/AndroidAssetStudio/index.html)
- [Icon Size Generator](http://realfavicongenerator.net/)

### References

- [Apple Developer Site](https://developer.apple.com/library/ios/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)
- [Web App Manifest](https://developers.google.com/web/fundamentals/web-app-manifest/)
- [UC Browser](http://www.uc.cn/download/UCBrowser_U3_API.doc)
- [Microsoft Internet Explorer](https://github.com/joshbuchea/HEAD#microsoft-internet-explorer)
- [PWACompat](https://github.com/GoogleChromeLabs/pwacompat) - to add support for splash screen in any device.

#### Contributions

- If you wish to contribute to this repository, fork it and send a PR 😬.
- And, if you like the repo, 🌟 it.

##### MIT Licensed
