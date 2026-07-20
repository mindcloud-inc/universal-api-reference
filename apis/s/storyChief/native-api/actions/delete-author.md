# Delete Author with StoryChief

Deletes an author from StoryChief.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/authors/:authorId`
- **Base URL:** `https://api.storychief.io/1.0`
- **Official documentation:** [Delete Author](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-b6585c71-de4c-427f-beac-2f8ea8f4e383)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authorId` | path | `number` | yes | Author identifier from the path. |
| `replacement_author_id` | query | `number` | yes | Replacement author ID documented for deleting an author. |
