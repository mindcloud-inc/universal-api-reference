# Analyze Object with Moderation API

Submits an object to Moderation API for analysis.

## Endpoint

- **Method:** `POST`
- **Path:** `/moderate/object`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Analyze Object](https://docs.moderationapi.com/api-reference/moderate/analyze-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contentId` | body | `string` | no | The unique ID of the content in your database. |
| `channelKey` | body | `string` | no | The key of the channel. |
| `doNotStore` | body | `boolean` | no | Do not store the content. The content won't enter the review queue |
| `authorId` | body | `string` | no | The author of the content. |
| `contextId` | body | `string` | no | For example the ID of a chat room or a post |
| `metadata` | body | `object` | no | Any metadata you want to store with the content |
| `value` | body | `object` | yes | The object you want to analyze. |
