# Create Webhook with Port API AI

Creates a webhook in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Create Webhook](https://docs.port.io/api-reference/create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | body | `string` | yes | The webhook identifier. |
| `title` | body | `string` | yes | The webhook title. |
| `enabled` | body | `boolean` | no | Whether the webhook is enabled. |
| `mappings[]` | body | `array<object>` | yes | Webhook mappings configuration. |
| `security` | body | `object` | no | Webhook security configuration. |
