# Get IP Geolocation with BigDataCloud

Retrieves IP geolocation details from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/ip-geolocation`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get IP Geolocation](https://www.bigdatacloud.com/ip-geolocation/ip-address-geolocation-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | no | If omitted, BigDataCloud uses the caller IP address. |
| `localityLanguage` | query | `string` | no | Preferred language for locality names in ISO 639-1 format. |
