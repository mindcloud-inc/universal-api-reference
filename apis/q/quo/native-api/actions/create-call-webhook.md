# Create Call Webhook with Quo

Creates a new webhook for Quo calls.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/calls`
- **Base URL:** `https://api.openphone.com/v1`
- **Official documentation:** [Create Call Webhook](https://www.quo.com/docs/mdx/api-reference/webhooks/create-a-new-webhook-for-calls)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes |
| `url` | body | `string` | yes |
| `label` | body | `string` | no |
| `resourceIds[]` | body | `array<string>` | no |
| `status` | body | `string` | no |
| `userId` | body | `string` | no |
