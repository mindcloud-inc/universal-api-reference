# Get ASN Info with BigDataCloud

Retrieves ASN details from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/asn-info`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get ASN Info](https://www.bigdatacloud.com/ip-geolocation/asn-short-info-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asn` | query | `string` | no | Autonomous system number in numeric, AS, or ASN format. |
| `localityLanguage` | query | `string` | no | Preferred language for locality names in ISO 639-1 format. |
