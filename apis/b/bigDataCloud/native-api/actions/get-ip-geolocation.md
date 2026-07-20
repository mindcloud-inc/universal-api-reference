# Get IP Geolocation Report with BigDataCloud

Retrieves IP geolocation, confidence area, and hazard details from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/ip-geolocation-full`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get IP Geolocation Report](https://www.bigdatacloud.com/ip-geolocation/ip-address-geolocation-with-confidence-area-and-hazard-report-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | no | If omitted, BigDataCloud uses the caller IP address. |
| `localityLanguage` | query | `string` | no | ISO 639-1 language code used for locality names. |
