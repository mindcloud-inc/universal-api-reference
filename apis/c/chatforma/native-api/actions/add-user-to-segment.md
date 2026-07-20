# Add User To Segment with Chatforma

Adds a user to a Chatforma segment.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/segments/:segmentId/users`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Add User To Segment](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `botId` | path | `number` | yes |
| `segmentId` | path | `number` | yes |
| `botUserId` | body | `number` | yes |
