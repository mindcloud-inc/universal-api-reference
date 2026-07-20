# Get bank statement content with Atlar

Retrieves bank statement content from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/connectivity/v2beta/connections/{cid}/reports/{rid}/bank-statements/{id}/content`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Get bank statement content](https://docs.atlar.com/reference/get-connectivity-v2beta-connections-cid-reports-rid-bank-statements-id-content)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cid` | path | `string<string>` | yes |
| `rid` | path | `string<string>` | yes |
| `id` | path | `string<string>` | yes |
| `format` | query | `string<string>` | no |
| `externalIdAsEndToEndId` | query | `boolean<string>` | no |
