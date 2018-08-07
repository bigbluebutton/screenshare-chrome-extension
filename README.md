# BigBlueButton Screenshare Chrome Extension

By default Google Chrome does not allow sharing of your computer screen. In order for the WebRTC Screenshare to work in BigBlueButton on Google Chrome, you need to whitelist your domain(s). This way Google Chrome will permit sharing your screen.

Everyone who is planning on sharing their screen in Google Chrome on BigBlueButton 2.0 using WebRTC will need to have an extension added. This set of instructions indicates how to whitelist your [institution's] domain(s) and publish the resulting extension to Google's extensions store.

In most use cases, a presenter will only need to add the extension from the Google Chrome store once.
BigBlueButton administrators will need to create such 

# Instructions for presenters

Just add the Google Chrome extension provided from your institution to your browser. It should look like 
https://chrome.google.com/webstore/detail/bigbluebutton-screenshare/<some unique identifier>

# Instructions for administrators for pushing a [newer] version of the Chrome Extension to the Google Store:

Download a copy of the files in this reposiory. Add the correct domain(s) for your institution in `manifest.json`.

```
"externally_connectable": {
   "matches": [
       "*://*.bigbluebutton.org/*",
       "*://*.YOUR_DOMAIN.com/*"
     ]
````

Bump up the version of the extension in `manifest.json` and save all files.

Navigate to chrome://extensions/ in Google Chrome. Enable 'Developer Mode' via the checkmark. Remove any existing versions of this extension. Select `Load unpacked extension...` and navigate to the folder containing manifest.json

If you are able to use this unpacked extension and it is working correctly, it is now safe to upload it to the Chrome WebStore.

Create a ZIP archive of the files in this directory (you can omit README.md)

```
screenshare-chrome-extension
├── background-script.js
├── icon.png
└── manifest.json
```


Sign in https://chrome.google.com/webstore/developer/ with Google developer user id
and upload the ZIP archive

After about 30-60 minutes the version of the application will be increased, indicating that the publishing of a new version was successful. Remove the unpacked version of the extension in your browser and install the packed version from the WebStore:

LINK = https://chrome.google.com/webstore/detail/bigbluebutton-screenshare/<KEY>

You should have a link to your extension now and a key.
You can populate the `kurento` section of the settings for screensharing with

```
"chromeExtensionKey": "KEY",
"chromeExtensionLink": "LINK"
```

Link:
https://chrome.google.com/webstore/detail/bigbluebutton-screenshare/akgoaoikmbmhcopjgakkcepdgdgkjfbc

