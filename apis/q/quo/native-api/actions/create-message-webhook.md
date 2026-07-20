# Create Message Webhook with Quo

Creates a new webhook for Quo messages.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/messages`
- **Base URL:** `https://api.openphone.com/v1`
- **Official documentation:** [Create Message Webhook](https://www.quo.com/docs/mdx/api-reference/webhooks/create-a-new-webhook-for-messages)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes |
| `label` | body | `string` | no |
| `resourceIds[]` | body | `array<string>` | no |
| `status` | body | `string` | no |
| `url` | body | `string` | yes |
| `userId` | body | `string` | no |
