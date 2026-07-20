# Read Webhook with BulkSMS

Retrieves a webhook from BulkSMS by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://api.bulksms.com/v1`
- **Official documentation:** [Read Webhook](https://www.bulksms.com/developer/json/v1/#tag/webhooks/GET/webhooks/{id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The webhook ID to retrieve. |
