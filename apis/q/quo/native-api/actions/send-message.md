# Send Message with Quo

Sends a text message in Quo.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://api.openphone.com/v1`
- **Official documentation:** [Send Message](https://www.quo.com/docs/mdx/api-reference/messages/send-a-text-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `content` | body | `string` | yes |
| `from` | body | `string` | no |
| `phoneNumberId` | body | `string` | no |
| `setInboxStatus` | body | `string` | no |
| `to[]` | body | `array<string>` | yes |
| `userId` | body | `string` | no |
