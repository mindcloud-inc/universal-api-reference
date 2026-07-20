# Create Webhook with Dubble

Creates a new webhook in Dubble.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.dubble.so/v1`
- **Official documentation:** [Create Webhook](https://dubble.readme.io/reference/post_webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional name for the webhook |
| `target_url` | body | `string` | yes | The URL where the webhook will send data |
| `triggers[]` | body | `array<string>` | yes | Trigger events for the webhook |
