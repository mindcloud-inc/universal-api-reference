# Create Post with BlogIn

Creates a new post in BlogIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts`
- **Base URL:** `https://blogin.co/api/rest`
- **Official documentation:** [Create Post](https://blogin.co/api/rest/docs/#create-new-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The title of the post. |
| `text` | body | `string` | yes | The HTML text of the post. |
| `author.id` | body | `number` | yes | The ID of the author of the post. |
| `published` | body | `boolean` | no | Whether the post is published. |
