# Create Dispatch To Segment with Chatforma

Creates a segment dispatch in Chatforma.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/segments/:segmentId/dispatch`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Create Dispatch To Segment](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `number` | yes | — |
| `segmentId` | path | `number` | yes | Use `0` to dispatch to all users for the bot. |
| `content` | body | `string` | yes | — |
