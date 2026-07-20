# Create Webhook Integration with OpnForm

Creates a webhook integration in OpnForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/open/forms/:formId/integrations`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Create Webhook Integration](https://docs.opnform.com/api-reference/integrations/create-webhook-integration)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `formId` | path | `number` | yes |
| `status` | body | `string` | yes |
| `data.webhook_url` | body | `string` | yes |
| `data.webhook_secret` | body | `string` | no |
| `data.webhook_headers` | body | `object` | no |
| `logic` | body | `object` | no |
