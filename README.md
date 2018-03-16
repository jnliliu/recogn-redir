# Device Recognition Redirector
PHP web site that collects information about the target device with just one click (e.g.: ip and headers, geo location, browser info, software and hardware info).
## How to use
### Parameters
**Required**

* **r** - URL (to redirect after collect information from the target device).
* **k** - Google maps api key (used for [Google Maps Geolocation API](https://developers.google.com/maps/documentation/geolocation/intro)).

**Optional**

* **i** - Request name or id to identify the target (all files will be created with this name. Default: random unique id).
* **og-[*]** - [Open Graph Protocol metadata](http://ogp.me) (show link as a rich object in a social graph).

### Example:
```
http://example.site?r=[URL_TO_REDIRECT]&k=[MAPS_API_KEY]&i=[TARGET_NAME]&og-url=[LINK_TO_SHOW_IN_SOCIAL_MEDIA]
```

### Collected Data
The target device information will be stored in three JSON files inside directory: _data/[**i**]/

* **request_info.json** - Contains information about the HTTP request. (target IP, all headers, etc).
* **device_info.json** - Contains information about the target device (OS, hardware, browser, etc).
* **geolocation.json** - Contains the target geolocation returned from [Google Maps Geolocation API](https://developers.google.com/maps/documentation/geolocation/intro).
