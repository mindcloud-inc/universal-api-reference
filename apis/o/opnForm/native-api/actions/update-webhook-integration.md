# Update Webhook Integration with OpnForm

Updates an existing webhook integration in OpnForm.

## Endpoint

- **Method:** `PUT`
- **Path:** `/open/forms/:formId/integrations/:integrationId`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Update Webhook Integration](https://docs.opnform.com/api-reference/integrations/update-webhook-integration)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `formId` | path | `number` | yes |
| `integrationId` | path | `number` | yes |
| `status` | body | `string` | yes |
| `data.webhook_url` | body | `string` | yes |
| `data.webhook_secret` | body | `string` | no |
| `data.webhook_headers` | body | `object` | no |
| `logic` | body | `object` | no |
