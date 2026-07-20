# List Mailings with CleverReach

Retrieves mailings from your CleverReach account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/mailings.json`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [List Mailings](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/mailings-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | number of items. |
| `state` | query | `string` | no | state of mailing. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `channel_id` | query | `string` | no | (optional): if specified, it will only return matching results. |
| `start` | query | `number` | no | (optional) Filter by start time (see note). |
| `end` | query | `number` | no | (optional) Filter by end time (see note). |
