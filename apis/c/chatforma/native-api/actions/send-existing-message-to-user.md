# Send Existing Message To User with Chatforma

Sends an existing message to a Chatforma user.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/user/:botUserId/message/:messageId`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Send Existing Message To User](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `botId` | path | `number` | yes |
| `botUserId` | path | `number` | yes |
| `messageId` | path | `string` | yes |
