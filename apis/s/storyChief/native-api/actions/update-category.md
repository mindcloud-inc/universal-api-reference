# Update Category with StoryChief

Updates an existing category in StoryChief.

## Endpoint

- **Method:** `PUT`
- **Path:** `/categories/:categoryId`
- **Base URL:** `https://api.storychief.io/1.0`
- **Official documentation:** [Update Category](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-c5ffbb34-b1b3-4224-addc-68031bf33945)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | path | `number` | yes | Category identifier from the path. |
| `name` | body | `string` | no | Updated category name. |
