Accounts Facebook Cordova
================

## Introduction

This packages replaces the accounts-facebook package. It works with [phonegap-facebook-plugin](https://github.com/phonegap/phonegap-facebook-plugin) when using cordova and falls back to the facebook package when in a browser. 

*Note: Currently only tested with iOS. Will test the other platforms asap.*

*Current status: Login works great! Working on abstracting the graph api calls so they work from both native sdk or http request .. although it may be better to just stick with http.*

================

## Installation / Setup

##### Requirements
* [Cordova: 3.5](http://cordova.apache.org/)
* [phonegap-facebook-plugin](https://github.com/phonegap/phonegap-facebook-plugin)

================

##### Package Installation
````
mrt add accounts-facebook-cordova
````
*Note: For testing you can also add accounts-ui package.*



================

##### Meteor settings file (settings.json)
````
{
  "facebook": {
    "appId": "[app_id]",
    "secret": "[app_secret]"
  },
  "public": {
    "facebook": {
      "permissions": [
        "public_profile", 
        "user_interests", 
        "user_activities", 
        "read_friendlists"
      ], 
      "profileFields": [
        "name",
        "gender",
        "location"
      ]     
    }
  }
}
````
================

### Cordova Setup Guide
Refer to the [phonegap-facebook-plugin readme](https://github.com/phonegap/phonegap-facebook-plugin)

## Final Notes

##### Running your app with settings
````
mrt --settings settings.json
````
================

If you want more features than this provides, file an issue. Feature requests/contributions are welcome.
