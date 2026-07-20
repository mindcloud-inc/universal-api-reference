# Create Webhook with Lettr

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://app.lettr.com/api/`
- **Official documentation:** [Create Webhook](https://docs.lettr.com/api-reference/webhooks/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_type` | body | `string` | yes | Webhook authentication type. |
| `events_mode` | body | `string` | yes | Whether to receive all or selected events. |
| `events[]` | body | `array<string>` | yes | Webhook event subscriptions. |
| `name` | body | `string` | yes | Webhook name. |
| `url` | body | `string` | yes | Webhook target URL. |
