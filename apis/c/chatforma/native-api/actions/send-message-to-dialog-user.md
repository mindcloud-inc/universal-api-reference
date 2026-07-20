# Send Message To Dialog User with Chatforma

Creates a dialog message for a Chatforma user.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/dialogs/:userId/message`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Send Message To Dialog User](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `botId` | path | `number` | yes |
| `userId` | path | `number` | yes |
| `message` | body | `string` | yes |
| `uid` | body | `string` | yes |
