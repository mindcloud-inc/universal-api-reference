# Delete Webhook with Moaform

Deletes a webhook from a form in Moaform.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/forms/:formId/webhooks/:webhookId`
- **Base URL:** `https://api.moaform.com/v1`
- **Official documentation:** [Delete Webhook](https://help.moaform.com/hc/en-us/articles/28337019205529-Deleting-Webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | Unique ID of the form. |
| `webhook_id` | path | `string` | yes | Unique ID of the webhook. |
