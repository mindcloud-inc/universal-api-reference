# Get report content with Atlar

Retrieves report content from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/connectivity/v2beta/connections/{cid}/reports/{id}/content`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Get report content](https://docs.atlar.com/reference/get-connectivity-v2beta-connections-cid-reports-id-content)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cid` | path | `string<string>` | yes |
| `id` | path | `string<string>` | yes |
| `format` | query | `string<string>` | no |
| `externalIdAsEndToEndId` | query | `boolean<string>` | no |
