# Submit Content For Moderation with Moderation API

Submits content to Moderation API for moderation.

## Endpoint

- **Method:** `POST`
- **Path:** `/moderate`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Submit Content For Moderation](https://docs.moderationapi.com/content-moderation/submit-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `object` | yes | The content sent for moderation |
| `timestamp` | body | `number` | no | Unix timestamp (in milliseconds) of when the content was created. Use if content is not submitted in real-time. |
| `channel` | body | `string` | no | Provide a channel ID or key. Will use the project's default channel if not provided. |
| `contentId` | body | `string` | no | The unique ID of the content in your database. |
| `metaType` | body | `string` | no | The meta type of content being moderated |
| `authorId` | body | `string` | no | The author of the content. |
| `conversationId` | body | `string` | no | For example the ID of a chat room or a post |
| `metadata` | body | `object` | no | Any metadata you want to store with the content |
| `doNotStore` | body | `boolean` | no | Do not store the content. The content won't enter the review queue |
| `policies[]` | body | `array<object>` | no | (Enterprise) override the channel policies for this moderation request only. |
