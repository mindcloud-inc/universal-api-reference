# Toggle Outgoing Webhook Status with Uspacy

Updates an outgoing webhook status in Uspacy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/company/v1/webhooks/:webhookId/toggle`
- **Base URL:** `https://{site}`
- **Official documentation:** [Toggle Outgoing Webhook Status](https://uspacy.readme.io/reference/patch_company-v1-webhooks-webhookid-toggle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | The outgoing webhook ID. |
