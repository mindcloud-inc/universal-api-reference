# Get ASN Info Extended with BigDataCloud

Retrieves extended ASN details from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/asn-info-full`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get ASN Info Extended](https://www.bigdatacloud.com/network-engineering/asn-info-extended-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asn` | query | `string` | no | Autonomous System Number as numeric or ASN format, for example 123, AS123, or ASN123. |
| `localityLanguage` | query | `string` | no | Preferred language for localized place and country names. |
| `peersCap` | query | `number` | no | Maximum number of receivingFrom and transitTo entries to retrieve. Default and hard limit are 50. |
