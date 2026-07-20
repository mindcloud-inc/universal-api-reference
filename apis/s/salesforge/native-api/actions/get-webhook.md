# Get Webhook with Salesforge

Retrieves a webhook from Salesforge.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v2/workspaces/:workspaceID/integrations/webhooks/:webhookID`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Get Webhook](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes |
| `webhookID` | path | `string` | yes |
