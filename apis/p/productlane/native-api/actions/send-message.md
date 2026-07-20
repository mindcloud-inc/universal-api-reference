# Send Message with Productlane

Creates a message in a Productlane thread.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads/:threadId/messages`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Send Message](https://productlane.mintlify.dev/docs/api/threads/send-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `threadId` | path | `string` | yes |
| `content` | body | `string` | yes |
| `cc[]` | body | `array<object>` | no |
| `bcc[]` | body | `array<object>` | no |
| `attachments[]` | body | `array<object>` | no |
| `channelId` | body | `string` | no |
