# Get Country Info with BigDataCloud

Retrieves country information from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/country-info`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get Country Info](https://www.bigdatacloud.com/ip-geolocation/country-info-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | query | `string` | no | Country code in ISO 3166-1 Alpha-2, Alpha-3, or numeric format. |
| `localityLanguage` | query | `string` | no | Preferred language for locality names in ISO 639-1 format. |
