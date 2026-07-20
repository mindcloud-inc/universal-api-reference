# Get Call Statistics with Novofon

Retrieves call statistics from Novofon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/statistics/`
- **Base URL:** `https://api.novofon.com`
- **Official documentation:** [Get Call Statistics](https://novofon.com/instructions/api/#statistics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cost_only` | query | `string` | no | Optional provider flag to return only spent cost for the selected period. |
| `end` | query | `string` | no | Optional statistics window end in `YYYY-MM-DD HH:MM:SS` format. |
| `limit` | query | `string` | no | Optional maximum number of rows to return. Docs say the provider maximum is 1000. |
| `sip` | query | `string` | no | Optional SIP number filter. |
| `skip` | query | `string` | no | Optional number of rows to skip for pagination. |
| `start` | query | `string` | no | Optional statistics window start in `YYYY-MM-DD HH:MM:SS` format. |
| `type` | query | `string` | no | Optional provider statistics type such as `toll` or `ru495`. Leave empty for the default overall statistics. |
