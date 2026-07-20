# List bank statements with Atlar

Retrieves bank statements from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/connectivity/v2beta/connections/{cid}/reports/{id}/bank-statements`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List bank statements](https://docs.atlar.com/reference/get-connectivity-v2beta-connections-cid-reports-id-bank-statements)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cid` | path | `string<string>` | yes |
| `id` | path | `string<string>` | yes |
| `account_id` | query | `string<string>` | no |
| `type` | query | `string<string>` | no |
| `from` | query | `date<string>` | no |
| `to` | query | `date<string>` | no |
