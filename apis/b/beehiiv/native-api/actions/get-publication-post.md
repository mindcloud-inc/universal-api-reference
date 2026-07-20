# Get Publication Post with Beehiiv

Retrieves a publication post from Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/posts/:postId`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Get Publication Post](https://developers.beehiiv.com/api-reference/posts/show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `postId` | path | `string` | yes | The prefixed ID of the post object. |
