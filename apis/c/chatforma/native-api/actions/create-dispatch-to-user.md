# Create Dispatch To User with Chatforma

Creates a user dispatch in Chatforma.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/dispatch/user/:botUserId`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Create Dispatch To User](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `number` | yes | — |
| `botUserId` | path | `number` | yes | — |
| `content` | body | `string` | yes | — |
| `run_at` | body | `string` | no | Start date; if omitted, Chatforma dispatches immediately. |
