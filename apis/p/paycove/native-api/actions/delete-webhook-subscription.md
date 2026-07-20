# Delete Webhook Subscription with Paycove

Deletes a webhook subscription from Paycove.

## Endpoint

- **Method:** `DELETE`
- **Path:** `hooks`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Delete Webhook Subscription](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_url` | body | `string` | yes | Target webhook URL to delete. |
| `event` | body | `string` | yes | Webhook event type to delete. |
