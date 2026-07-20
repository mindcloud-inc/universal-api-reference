# Create Document with Formstack Documents

Creates a new document in Formstack Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Create Document](https://www.webmerge.me/developers/documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_contents` | body | `string` | no | Base64-encoded source file contents |
| `file_url` | body | `string` | no | Public URL for the source file |
| `folder` | body | `string` | no | Folder name to save the document in |
| `html` | body | `string` | no | HTML content for HTML documents |
| `name` | body | `string` | yes | Name of the document |
| `output` | body | `string` | yes | Output format to produce when merged |
| `output_name` | body | `string` | no | Custom filename for merged output |
| `type` | body | `string` | yes | Source document type |
