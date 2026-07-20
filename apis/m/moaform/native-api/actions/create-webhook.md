# Create Webhook with Moaform

Creates a webhook for a form in Moaform.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/webhooks`
- **Base URL:** `https://api.moaform.com/v1`
- **Official documentation:** [Create Webhook](https://help.moaform.com/hc/en-us/articles/28335977118745-Create-a-New-Webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | Unique ID of the form. |
| `endpoint` | body | `string` | yes | Webhook receiver URL. |
| `enabled` | body | `boolean` | no | Webhook activation status. |
| `secret` | body | `string` | no | Secret code for signing webhook payloads. |
| `verify_ssl` | body | `boolean` | no | Whether to verify the endpoint SSL certificate. |
| `retention_days` | body | `number` | no | Resend restriction days. |
