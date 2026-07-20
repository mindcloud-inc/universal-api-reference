# Update Story with StoryChief

Updates an existing story in StoryChief.

## Endpoint

- **Method:** `PUT`
- **Path:** `/stories/:storyId`
- **Base URL:** `https://api.storychief.io/1.0`
- **Official documentation:** [Update Story](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-ce0be312-48b9-4f2c-b248-f86d98a765ec)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author_id` | body | `string` | no | Updated author ID for the story. |
| `content` | body | `string` | no | Updated story HTML content. |
| `excerpt` | body | `string` | no | Updated story excerpt. |
| `slug` | body | `string` | no | Updated story slug. |
| `storyId` | path | `number` | yes | Story identifier from the path. |
| `title` | body | `string` | no | Updated story title. |
