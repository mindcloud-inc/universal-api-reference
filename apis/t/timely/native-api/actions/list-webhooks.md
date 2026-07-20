# List Webhooks with Timely

Retrieves webhooks from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/webhooks`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [List Webhooks](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `limit` | query | `number` | no | Maximum number of webhooks to return |
| `offset` | query | `number` | no | Number of webhooks to skip |
