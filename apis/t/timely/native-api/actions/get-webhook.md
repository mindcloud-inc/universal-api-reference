# Get Webhook with Timely

Retrieves a webhook from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/webhooks/{id}`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Get Webhook](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `id` | path | `number` | yes | Webhook ID |
