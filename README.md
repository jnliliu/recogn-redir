# Device Recognition Redirector
PHP web site that collects information about the target device with just one click (e.g.: IP, headers, geo location, browser info, software and hardware info).
## How to use
Copy the **index.php** file to server, build the link (see example) and send it to target.

### Parameters
**Required**

* **r** - URL (to redirect after collect information from the target device).
* **k** - Google maps api key (used for [Google Maps Geolocation API](https://developers.google.com/maps/documentation/geolocation/intro)).

**Optional**

* **i** - Request name or ID to identify the target (all files will be created with this name. Default: random unique id).
* **og-[*]** - [Open Graph Protocol metadata](http://ogp.me) (show link as a rich object in a social graph).

### Example:
```
http://example.site?r=[URL_TO_REDIRECT]&k=[MAPS_API_KEY]&i=[TARGET_NAME]&og-url=[LINK_TO_SHOW_IN_SOCIAL_MEDIA]
```

### Device Data
The script creates the following three files per request (or appends if the [i] - target ID already exists) in:
Path: "**_data/[i]/**"

* **request_info.json** - Contains information about the HTTP request. (target IP, all headers, etc).
* **device_info.json** - Contains information about the target device (OS, hardware, browser, etc).
* **geolocation.json** - Contains the target geolocation returned from [Google Maps Geolocation API](https://developers.google.com/maps/documentation/geolocation/intro).

### Copyrigth ©
This project includes:
* [**UAParser.js**](https://github.com/faisalman/ua-parser-js) - Copyright © 2012-2016 Faisal Salman <fyzlman@gmail.com>
