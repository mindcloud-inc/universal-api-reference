# Send Existing Message To Segment with Chatforma

Sends an existing message to a Chatforma segment.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/segments/:segmentId/message/:messageId`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Send Existing Message To Segment](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `number` | yes | — |
| `segmentId` | path | `number` | yes | — |
| `messageId` | path | `string` | yes | — |
| `run_at` | body | `string` | no | Start date; if omitted, Chatforma sends immediately. |
