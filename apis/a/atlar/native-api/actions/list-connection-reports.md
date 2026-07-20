# List connection reports with Atlar

Retrieves connection reports from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/connectivity/v2beta/connections/{cid}/reports`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List connection reports](https://docs.atlar.com/reference/get-connectivity-v2beta-connections-cid-reports)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cid` | path | `string<string>` | yes |
| `type` | query | `string<string>` | no |
| `statementType` | query | `string<string>` | no |
