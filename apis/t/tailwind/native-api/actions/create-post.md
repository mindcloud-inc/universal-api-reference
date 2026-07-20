# Create Post with Tailwind

Creates a new post in Tailwind.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:accountId/posts`
- **Base URL:** `https://api-v1.tailwind.ai`
- **Official documentation:** [Create Post](https://api-docs.tailwind.ai/rest-api/operations/v1accountsaccountidposts/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Pinterest account ID. |
| `mediaUrl` | body | `string` | yes | Publicly accessible image or video URL to pin. |
| `mediaType` | body | `string` | no | Media type. Defaults to image. Accepted values: `0`, `1`. |
| `title` | body | `string` | no | Pin title. Required when scheduling via sendAt. |
| `description` | body | `string` | no | Pin description. Required when scheduling via sendAt. |
| `url` | body | `string` | no | Destination URL when the pin is clicked. Required when scheduling via sendAt. |
| `boardId` | body | `string` | no | Target board ID. Required when scheduling via sendAt. |
| `altText` | body | `string` | no | Alt text for accessibility. |
| `sendAt` | body | `date` | no | ISO 8601 time to schedule the post. If omitted, the post is saved as a draft. |
| `isSimplifiedPin` | body | `boolean` | no | Whether to create a simplified pin. Defaults to true. |
