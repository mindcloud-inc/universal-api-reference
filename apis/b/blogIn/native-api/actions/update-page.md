# Update Page with BlogIn

Updates an existing page in BlogIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/pages/:id`
- **Base URL:** `https://blogin.co/api/rest`
- **Official documentation:** [Update Page](https://blogin.co/api/rest/docs/#update-a-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the page to update. |
| `title` | body | `string` | yes | The title of the page. |
| `text` | body | `string` | no | The HTML text of the page. |
| `author.id` | body | `number` | yes | The ID of the author of the page. |
| `published` | body | `boolean` | no | Whether the page is published. |
| `position` | body | `number` | no | The sort position of the page. |
