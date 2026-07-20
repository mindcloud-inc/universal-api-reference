# Update User with StoryChief

Updates an existing user in StoryChief.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:userId`
- **Base URL:** `https://api.storychief.io/1.0`
- **Official documentation:** [Update User](https://www.postman.com/storychief/storychief-s-public-workspace/documentation/bvzysnr/storychief-api?entity=request-3269417-270ccfe0-abf6-4d09-b09a-18c6dc78433e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | no | User phone number. |
| `userId` | path | `number` | yes | User identifier from the path. |
