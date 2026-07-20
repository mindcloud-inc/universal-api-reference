# Create Page with BlogIn

Creates a new page in BlogIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/pages`
- **Base URL:** `https://blogin.co/api/rest`
- **Official documentation:** [Create Page](https://blogin.co/api/rest/docs/#create-new-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The title of the page. |
| `text` | body | `string` | no | The HTML text of the page. |
| `author.id` | body | `number` | yes | The ID of the author of the page. |
| `published` | body | `boolean` | no | Whether the page is published. |
| `position` | body | `number` | no | The sort position of the page. |
