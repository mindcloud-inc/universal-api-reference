# Get Country by IP with BigDataCloud

Retrieves country details by IP address from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/country-by-ip`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get Country by IP](https://www.bigdatacloud.com/ip-geolocation/country-by-ip-address-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | no | If omitted, BigDataCloud uses the caller IP address. |
| `localityLanguage` | query | `string` | no | Preferred language for locality names in ISO 639-1 format. |
