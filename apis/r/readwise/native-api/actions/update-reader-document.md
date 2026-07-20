# Update Reader Document with Readwise

Updates an existing document in Readwise Reader.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/update/:documentId/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Update Reader Document](https://readwise.io/reader_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The Readwise Reader document ID to update. |
| `title` | body | `string` | no | The document title to overwrite the current title. |
| `author` | body | `string` | no | The document author to overwrite the current author. |
| `summary` | body | `string` | no | Summary of the document. |
| `published_date` | body | `string` | no | Published datetime in ISO 8601 format. |
| `image_url` | body | `string` | no | Image URL to use as the cover image. |
| `seen` | body | `boolean` | no | Mark the document as seen or unseen. |
| `location` | body | `string` | no | Reader location for the document. |
| `category` | body | `string` | no | Reader category for the document. |
| `tags` | body | `list<string>` | no | List of tag strings to replace the current tags. |
| `notes` | body | `string` | no | Document note text. Pass an empty string to clear it. |
