# Get IP Geolocation with Confidence Area with BigDataCloud

Retrieves IP geolocation with confidence area details from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/ip-geolocation-with-confidence`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get IP Geolocation with Confidence Area](https://www.bigdatacloud.com/ip-geolocation/ip-address-geolocation-with-confidence-area-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | no | IPv4 or IPv6 address. If omitted, the caller IP address is assumed. |
| `localityLanguage` | query | `string` | no | Preferred language for locality names in ISO 639-1 format. |
