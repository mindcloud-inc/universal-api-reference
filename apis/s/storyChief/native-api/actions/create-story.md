# Create Story with StoryChief

Creates a new story in StoryChief.

## Endpoint

- **Method:** `POST`
- **Path:** `/stories`
- **Base URL:** `https://api.storychief.io/1.0`
- **Official documentation:** [Create Story](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-6cb1bcf5-5132-46b5-99b3-ae72705fbd2e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author_id` | body | `string` | no | Author ID for the story. |
| `content` | body | `string` | no | Story HTML content. |
| `excerpt` | body | `string` | no | Story excerpt. |
| `language` | body | `string` | no | Story language code. |
| `slug` | body | `string` | no | Story slug. |
| `source_id` | body | `string` | no | Source ID for the story. |
| `title` | body | `string` | no | Story title. |
