# Cordova Ionic Web View with Extra Logging
Additional logging added to a custom cordova-plugin-ionic-webview for iOS.

## About the logging
In iOS additional logging like:
#### `[[Damian-WV] shouldAllowRequest false anyPluginsResponded false for url:%@`
This indicates that no plugins responded and the request for the url was blocked


#### `[Damian-WV] shouldAllowRequest false scheme fail %@ for url:%@`
This indicates that request will fail because of the scheme used


#### `[Damian-WV] shouldAllowRequest false for url:%@ plugin:%@`
This indicates that the request will fail because the url was blocked by a plugin

## Testing
Test by:
- `npm install`
- `ionic cordova build ios`

## Add to your app
Incorporate in your application by:
- Copy the folder `cordova-plugin-ionic-webview` into your project
- Alter `package.json` to use this custom plugin:
`"cordova-plugin-ionic-webview": "file:cordova-plugin-ionic-webview",`
- Run `npm install`
Then for good measure re-add your platforms: 
eg: `rm -rf platforms`, `rm -rf plugins` then `ionic cordova platform add ios@6.2` and `ionic cordova platform add android@10`
