# Update Author with StoryChief

Updates an existing author in StoryChief.

## Endpoint

- **Method:** `PUT`
- **Path:** `/authors/:authorId`
- **Base URL:** `https://api.storychief.io/1.0`
- **Official documentation:** [Update Author](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-834f48fd-2bc1-4559-9dee-fe0780d3e9be)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authorId` | path | `number` | yes | Author identifier from the path. |
| `bio` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `facebook_link` | body | `string` | no | Author Facebook profile URL. |
| `firstname` | body | `string` | no | — |
| `lastname` | body | `string` | no | — |
