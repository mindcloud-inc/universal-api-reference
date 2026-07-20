# Update Post with BlogIn

Updates an existing post in BlogIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/:id`
- **Base URL:** `https://blogin.co/api/rest`
- **Official documentation:** [Update Post](https://blogin.co/api/rest/docs/#update-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the post to update. |
| `title` | body | `string` | yes | The title of the post. |
| `text` | body | `string` | yes | The HTML text of the post. |
| `author.id` | body | `number` | yes | The ID of the author of the post. |
| `published` | body | `boolean` | no | Whether the post is published. |
