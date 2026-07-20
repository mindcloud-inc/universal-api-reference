# Update Webhook with Dubble

Updates an existing webhook in Dubble.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/:webhookId`
- **Base URL:** `https://api.dubble.so/v1`
- **Official documentation:** [Update Webhook](https://dubble.readme.io/reference/updatewebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional name for the webhook |
| `target_url` | body | `string` | no | The URL where the webhook will send data |
| `triggers[]` | body | `array<string>` | no | Trigger events for the webhook |
| `webhookId` | path | `string` | yes | The ID of the webhook |
