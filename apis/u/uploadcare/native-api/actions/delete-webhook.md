# Delete Webhook with Uploadcare

Deletes a webhook from Uploadcare by target URL.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhooks/unsubscribe/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Delete Webhook](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Webhook/operation/webhookUnsubscribe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_url` | body | `string` | yes | Webhook destination URL to unsubscribe. |
