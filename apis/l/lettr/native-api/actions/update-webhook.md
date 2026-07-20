# Update Webhook with Lettr

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/:webhookId`
- **Base URL:** `https://app.lettr.com/api/`
- **Official documentation:** [Update Webhook](https://docs.lettr.com/api-reference/webhooks/update-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | no | Whether the webhook is enabled. |
| `name` | body | `string` | no | Updated webhook name. |
| `target` | body | `string` | no | Updated webhook target URL. |
| `webhookId` | path | `string` | no | Webhook identifier. |
