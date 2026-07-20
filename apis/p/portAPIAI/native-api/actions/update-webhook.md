# Update Webhook with Port API AI

Updates a webhook in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/:identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Webhook](https://docs.port.io/api-reference/update-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The Port webhook identifier. |
| `title` | body | `string` | no | The updated webhook title. |
| `description` | body | `string` | no | The updated webhook description. |
| `enabled` | body | `boolean` | no | Whether the webhook is enabled. |
| `mappings[]` | body | `array<object>` | no | Webhook mappings configuration. |
