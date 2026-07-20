# Remove User From Segment with Chatforma

Deletes a user from a Chatforma segment.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/bots/:botId/segments/:segmentId/users`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Remove User From Segment](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `botId` | path | `number` | yes |
| `segmentId` | path | `number` | yes |
| `botUserId` | body | `number` | yes |
