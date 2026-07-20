# Delete Webhook with Resend

Deletes an existing webhook from Resend.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Delete Webhook](https://resend.com/docs/api-reference/webhooks/delete-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<string>` | yes | The unique identifier of the webhook to delete |
