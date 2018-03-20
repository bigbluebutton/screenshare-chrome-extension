# BBB-Screenshare-Chrome-Extension

# Instructions for pushing a newer version of the Chrome Extension:

[Make some changes in the files]
Bump up the version of the extension in `manifest.json` and save all files.


Navigate to chrome://extensions/ in Google Chrome. Enable 'Developer Mode' via the checkmark. Remove any existing versions of this extension. Select `Load unpacked extension...` and navigate to the folder containing manifest.json

If you are able to use this unpacked extension and it is working correctly, it is now safe to upload it to the Chrome WebStore.

Create a ZIP archive of the files in this directory (you can omit README.md)

```
BBB-Screenshare-Chrome-Extension
├── background-script.js
├── icon.png
└── manifest.json
```


Sign in https://chrome.google.com/webstore/developer/ with Google developer user id
and upload the ZIP archive

After about 30-60 minutes the version of the application will be increased, indicating that the publishing of a new version was successful. Remove the unpacked version of the extension in your browser and install the packed version from the WebStore:

https://chrome.google.com/webstore/detail/bigbluebutton-screenshare/<some unique identifier>
