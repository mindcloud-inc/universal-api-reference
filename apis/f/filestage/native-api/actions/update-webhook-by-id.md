# Update Webhook by ID with Filestage

Updates a webhook in Filestage by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/{webhookId}`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Update Webhook by ID](https://developers.filestage.io/docs/api/81v5wkyjfcm5t-update-webhook-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | The ID of the webhook |
| `webhookUrl` | body | `string` | no | — |
| `events[]` | body | `array<string>` | no | — |
| `headers` | body | `object` | no | — |
