# List Report Receivers by State with CleverReach

Retrieves report receivers from CleverReach by delivery state.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/reports.json/:id/receivers/:state`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [List Report Receivers by State](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/reports-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Report ID/Mailing ID. |
| `state` | path | `string` | yes | State to get. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `linkid` | query | `string` | no | ID of link that was clicked on. |
| `from` | query | `number` | no | Timestamp of earliest event of state. |
| `to` | query | `number` | no | Timestamp of latest event of state. |
| `detail` | query | `number` | no | Detail depth (bitwise combinable) (0: none, 1: events, 2: orders, 4: tags). |
| `pagesize` | query | `number` | no | Max items. |
| `page` | query | `number` | no | Page. |
