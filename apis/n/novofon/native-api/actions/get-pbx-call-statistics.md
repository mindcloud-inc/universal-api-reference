# Get PBX Call Statistics with Novofon

Retrieves PBX call statistics from Novofon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/statistics/pbx/`
- **Base URL:** `https://api.novofon.com`
- **Official documentation:** [Get PBX Call Statistics](https://novofon.com/instructions/api/#statistics_pbx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_type` | query | `string` | no | Optional call direction filter. Docs list `in` for inbound and `out` for outbound. |
| `end` | query | `string` | no | Optional statistics window end in `YYYY-MM-DD HH:MM:SS` format. |
| `limit` | query | `string` | no | Optional maximum number of rows to return. Docs say the provider maximum is 1000. |
| `skip` | query | `string` | no | Optional number of rows to skip for pagination. |
| `start` | query | `string` | no | Optional statistics window start in `YYYY-MM-DD HH:MM:SS` format. |
| `version` | query | `string` | yes | PBX statistics response format version. Docs list `2` as the new format and `1` as the old format. |
