# Update Webhook with Moaform

Updates a form webhook in Moaform.

## Endpoint

- **Method:** `PUT`
- **Path:** `/forms/:formId/webhooks/:webhookId`
- **Base URL:** `https://api.moaform.com/v1`
- **Official documentation:** [Update Webhook](https://help.moaform.com/hc/en-us/articles/28336903807897-Changing-Webhook-Settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | Unique ID of the form. |
| `webhook_id` | path | `string` | yes | Unique ID of the webhook. |
| `endpoint` | body | `string` | no | Webhook receiver URL. |
| `enabled` | body | `boolean` | no | Webhook activation status. |
| `secret` | body | `string` | no | Secret code for signing webhook payloads. |
| `verify_ssl` | body | `boolean` | no | Whether to verify the endpoint SSL certificate. |
| `retention_days` | body | `number` | no | Resend restriction days. |
