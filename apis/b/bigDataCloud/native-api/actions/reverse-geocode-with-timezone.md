# Reverse Geocode with Timezone with BigDataCloud

Reverse geocodes coordinates with timezone details in BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/reverse-geocode-with-timezone`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Reverse Geocode with Timezone](https://www.bigdatacloud.com/reverse-geocoding/reverse-geocode-with-timezone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | no | Latitude value in the WGS 84 reference system. |
| `longitude` | query | `number` | no | Longitude value in the WGS 84 reference system. |
| `localityLanguage` | query | `string` | no | Preferred language for locality names in ISO 639-1 format. |
