# Get Report Stats with CleverReach

Retrieves report statistics from CleverReach by reporting mode.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/reports.json/:id/stats/:mode`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [Get Report Stats](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/reports-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of Report/Mailing. |
| `mode` | path | `string` | no | Mode of statistics. Accepted values: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `start` | query | `string` | no | Startdate unixtimestamp (only for mode daily). |
| `end` | query | `string` | no | Enddate unixtimestamp (only for mode daily). |
