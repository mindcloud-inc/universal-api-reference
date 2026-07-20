# Create Webhook with Promptmate.io

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.promptmate.io/v1`
- **Official documentation:** [Create Webhook](https://apidoc.promptmate.io/api-5407074)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpointUrl` | body | `string` | yes | Destination URL Promptmate should call. |
| `restrictedAppIds[]` | body | `array<string>` | no | Optional list of Promptmate app IDs allowed to trigger the webhook. |
| `webhookName` | body | `string` | yes | Human-readable name for the webhook. |
| `webhookReference` | body | `string` | no | Optional caller-defined reference value. |
| `webhookType` | body | `string` | yes | Webhook event type. Promptmate currently documents job webhooks. |
