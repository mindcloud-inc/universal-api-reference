# Get Incoming Call Statistics with Novofon

Retrieves incoming call statistics from Novofon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/statistics/incoming-calls/`
- **Base URL:** `https://api.novofon.com`
- **Official documentation:** [Get Incoming Call Statistics](https://novofon.com/instructions/api/#statistics_incoming)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | Optional statistics window end in `YYYY-MM-DD HH:MM:SS` format. |
| `limit` | query | `string` | no | Optional maximum number of rows to return. Docs say the provider maximum is 1000. |
| `sip` | query | `string` | no | Optional SIP number filter. |
| `skip` | query | `string` | no | Optional number of rows to skip for pagination. |
| `start` | query | `string` | no | Optional statistics window start in `YYYY-MM-DD HH:MM:SS` format. |
