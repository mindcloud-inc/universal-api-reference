# Delete Webhook Integration with OpnForm

Deletes an existing webhook integration from OpnForm.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/open/forms/:formId/integrations/:integrationId`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Delete Webhook Integration](https://docs.opnform.com/api-reference/integrations/delete-webhook-integration)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `formId` | path | `number` | yes |
| `integrationId` | path | `number` | yes |
