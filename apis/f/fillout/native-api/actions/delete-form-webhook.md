# Delete Form Webhook with Fillout

Deletes a form webhook from Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/delete`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Delete Form Webhook](https://fillout.com/help/api-reference/remove-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | body | `string` | yes | The webhook identifier to remove. |
