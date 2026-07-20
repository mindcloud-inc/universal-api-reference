# Create Publication Post with Beehiiv

Creates a publication post in Beehiiv.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/publications/:publicationId/posts`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Create Publication Post](https://developers.beehiiv.com/api-reference/posts/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `title` | body | `string` | yes | Post title. |
| `body_content` | body | `string` | no | Raw HTML body content for the post. |
