# Create Post with StoryChief

Creates a new post in StoryChief.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts`
- **Base URL:** `https://api.storychief.io/1.0`
- **Official documentation:** [Create Post](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-c05bc757-65bc-40d7-80ca-062f5b4dd6f4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destinations` | body | `string` | no | Destination IDs for the post. |
| `due_at` | body | `string` | no | Scheduled due timestamp. |
| `message` | body | `string` | no | Post message. |
