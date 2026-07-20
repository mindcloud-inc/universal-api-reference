# Remove Webhook with Fillout Forms

Deletes a webhook from Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/delete`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Remove Webhook](https://www.fillout.com/help/api-reference/remove-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | body | `string` | yes | The webhook ID to remove. |
