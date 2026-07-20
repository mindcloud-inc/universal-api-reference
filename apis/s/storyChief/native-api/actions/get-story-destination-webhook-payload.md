# Get Story Destination Webhook Payload with StoryChief

Retrieves a story destination webhook payload from StoryChief.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories/:storyId/destinations/:destinationId/webhook`
- **Base URL:** `https://api.storychief.io/1.0`
- **Official documentation:** [Get Story Destination Webhook Payload](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-06b3e680-ea41-49d2-86bd-de63e6f49351)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destinationId` | path | `number` | yes | Destination identifier from the path. |
| `storyId` | path | `number` | yes | Story identifier from the path. |
