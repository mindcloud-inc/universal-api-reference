# Delete Webhook with BulkSMS

Deletes an existing webhook from BulkSMS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://api.bulksms.com/v1`
- **Official documentation:** [Delete Webhook](https://www.bulksms.com/developer/json/v1/#tag/webhooks/DELETE/webhooks/{id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The webhook ID to delete. |
