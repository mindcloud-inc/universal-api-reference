# Update Tag with StoryChief

Updates an existing tag in StoryChief.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tags/:tagId`
- **Base URL:** `https://api.storychief.io/1.0`
- **Official documentation:** [Update Tag](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-735a456b-9631-450d-b6e6-6a3d2492bb23)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Updated tag name. |
| `tagId` | path | `number` | yes | Tag identifier from the path. |
