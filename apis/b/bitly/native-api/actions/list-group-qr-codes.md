# List Group QR Codes with Bitly

Retrieves QR codes for a group in Bitly.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_guid/qr-codes`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [List Group QR Codes](https://dev.bitly.com/api-reference#listQRMinimal)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `group_guid` | path | `string` | yes |
| `size` | query | `number` | no |
