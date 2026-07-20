# Analyze Audio with Moderation API

Submits audio to Moderation API for analysis.

## Endpoint

- **Method:** `POST`
- **Path:** `/moderate/audio`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Analyze Audio](https://docs.moderationapi.com/api-reference/moderate/analyze-audio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contentId` | body | `string` | no | The unique ID of the content in your database. |
| `channelKey` | body | `string` | no | The key of the channel. |
| `doNotStore` | body | `boolean` | no | Do not store the content. The content won't enter the review queue |
| `authorId` | body | `string` | no | The author of the content. |
| `contextId` | body | `string` | no | For example the ID of a chat room or a post |
| `metadata` | body | `object` | no | Any metadata you want to store with the content |
| `url` | body | `string` | yes | The URL of the audio you want to analyze. |
