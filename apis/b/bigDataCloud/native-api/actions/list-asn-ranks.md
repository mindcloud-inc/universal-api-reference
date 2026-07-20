# List ASN Ranks with BigDataCloud

Retrieves ASN rank data from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/asn-rank-list`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [List ASN Ranks](https://www.bigdatacloud.com/network-engineering/asn-rank-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchSize` | query | `number` | no | Requested batch size. Maximum value is 1000. |
| `offset` | query | `number` | no | Number of entries to skip. |
| `sort` | query | `string` | no | Sort response by rank, asn, asnNumeric, organisation, or countryCode. |
| `order` | query | `string` | no | Sort order: asc or desc. |
| `localityLanguage` | query | `string` | no | Preferred language for localized country names. |
