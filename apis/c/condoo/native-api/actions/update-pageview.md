# Update Pageview with condoo

Updates an existing pageview in condoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/pageviews-lightweight/{event_id}`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [Update Pageview](https://trk.condoo.systems/en/api-documentation/pageviews-lightweight)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `browser_language` | body | `string` | no | Optional browser language, such as en. |
| `browser_name` | body | `string` | no | Optional browser name, such as Chrome. |
| `browser_timezone` | body | `string` | no | Optional browser timezone, such as UTC. |
| `city_name` | body | `string` | no | Optional city name. |
| `continent_code` | body | `string` | no | Optional continent code. Allowed values: AF, AN, AS, EU, NA, OC, SA. |
| `country_code` | body | `string` | no | Optional ISO country code. |
| `device_type` | body | `string` | no | Optional device type. Allowed values: desktop, mobile, tablet. |
| `event_id` | path | `number` | yes | Required pageview event ID. |
| `os_name` | body | `string` | no | Optional operating system name. |
| `path` | body | `string` | no | Optional page path. |
| `referrer_host` | body | `string` | no | Optional referrer host. |
| `referrer_path` | body | `string` | no | Optional referrer path, such as /page. |
| `screen_resolution` | body | `string` | no | Optional screen resolution. |
| `theme` | body | `string` | no | Optional theme. Allowed values: light, dark. |
| `type` | body | `string` | no | Optional type. Allowed values: pageview, custom. |
| `utm_campaign` | body | `string` | no | Optional UTM campaign. |
| `utm_medium` | body | `string` | no | Optional UTM medium. |
| `utm_source` | body | `string` | no | Optional UTM source. |
| `website_id` | body | `number` | no | Optional website ID. |
