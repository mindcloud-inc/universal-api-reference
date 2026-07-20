# Update Webhook with Fingertip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/webhooks/:webhookId`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Update Webhook](https://docs.fingertip.com/openapi-specs/update-webhook.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | ID of the webhook to update. |
| `endpointUrl` | body | `string` | no | Updated webhook destination URL. |
| `triggers[]` | body | `array<object>` | no | Updated webhook trigger definitions. |
