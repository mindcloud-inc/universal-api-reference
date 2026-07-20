# Get Network by IP with BigDataCloud

Retrieves network details by IP address from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/network-by-ip`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get Network by IP](https://www.bigdatacloud.com/ip-geolocation/network-by-ip-address-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | no | If omitted, BigDataCloud uses the caller IP address. |
| `localityLanguage` | query | `string` | no | Preferred language for locality names in ISO 639-1 format. |
