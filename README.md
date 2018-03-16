# Recognition Redirector

## How to use
### Parameters
**Required**

* **r** - URL (to redirect after collect information from the target device)
* **k** - Google maps api key (used for [Google Maps Geolocation API](https://developers.google.com/maps/documentation/geolocation/intro))

**Optional**

* **i** - Request name or id to identify the target (all files will be created with this name)
* **og-[*]** - [Open Graph Protocol metadata](http://ogp.me) (to show link as a rich object in a social graph)


### Example:
```
http://example.site?r=[URL_TO_REDIRECT]&k=[MAPS_API_KEY]&i=[TARGET_NAME]&og-url=[URL_TO_SHOW_IN_SOCIAL_MEDIA]
```
