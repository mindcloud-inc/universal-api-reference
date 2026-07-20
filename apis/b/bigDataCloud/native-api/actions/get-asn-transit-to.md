# Get ASN Transit To with BigDataCloud

Retrieves ASN transit-to information from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/asn-info-transit-to`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get ASN Transit To](https://www.bigdatacloud.com/network-engineering/asn-info-transit-to)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asn` | query | `string` | no | Autonomous System Number as numeric or ASN format. |
| `batchSize` | query | `number` | no | Number of transitTo entries to retrieve. Hard limit is 50. |
| `offset` | query | `number` | no | Number of transitTo entries to skip. |
| `localityLanguage` | query | `string` | no | Preferred language for localized country names. |
