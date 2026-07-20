# Delete Webhook with Seven

Deletes a webhook from Seven.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/hooks`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Delete Webhook](https://docs.seven.io/en/rest-api/endpoints/webhooks#delete-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | no | The ID of the webhook you want to delete. |
| `target_url` | body | `string` | no | Destination address of your webhook. |
| `event_type` | body | `string` | no | Type of event for which you would like to receive a webhook. |
| `request_method` | body | `string` | no | Request method in which you would like to receive the webhook. |
