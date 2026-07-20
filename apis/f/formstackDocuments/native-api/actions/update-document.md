# Update Document with Formstack Documents

Updates an existing document in Formstack Documents.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:id`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Update Document](https://www.webmerge.me/developers/documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_contents` | body | `string` | no | Updated base64-encoded file contents |
| `file_url` | body | `string` | no | Updated public file URL |
| `folder` | body | `string` | no | Updated folder name |
| `html` | body | `string` | no | Updated HTML content for HTML documents |
| `id` | path | `string` | yes | ID of the document to update |
| `name` | body | `string` | no | Updated document name |
| `output` | body | `string` | no | Updated output format |
| `output_name` | body | `string` | no | Updated merged filename |
