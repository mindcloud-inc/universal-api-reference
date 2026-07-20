# Get ASN Receiving From with BigDataCloud

Retrieves ASN receiving-from information from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/asn-info-receiving-from`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get ASN Receiving From](https://www.bigdatacloud.com/network-engineering/asn-info-receiving-from)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asn` | query | `string` | no | Autonomous System Number as numeric or ASN format. |
| `batchSize` | query | `number` | no | Number of receivingFrom entries to retrieve. Hard limit is 50. |
| `offset` | query | `number` | no | Number of receivingFrom entries to skip. |
| `localityLanguage` | query | `string` | no | Preferred language for localized country names. |
