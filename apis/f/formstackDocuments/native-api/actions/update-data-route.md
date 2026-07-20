# Update Data Route with Formstack Documents

Updates an existing data route in Formstack Documents.

## Endpoint

- **Method:** `PUT`
- **Path:** `/routes/:id`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Update Data Route](https://www.webmerge.me/developers/routes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder` | body | `string` | no | Updated folder name |
| `id` | path | `string` | yes | ID of the data route to update |
| `name` | body | `string` | no | Updated data route name |
| `output_name` | body | `string` | no | Updated custom filename for combined output |
| `rules[][combine_docx]` | body | `string` | no | Whether to include each rule in the combined DOCX |
| `rules[][combine]` | body | `string` | no | Whether to include each rule in the combined PDF |
| `rules[][document_id]` | body | `string` | no | Updated document ID for each rule |
| `rules[][file]` | body | `string` | no | Updated remote file URL or merge field for each rule |
| `rules[][id]` | body | `string` | no | Existing rule ID when updating a data route |
| `rules[][loop_field]` | body | `string` | no | Array field used to repeat a rule |
| `rules[][sort]` | body | `string` | no | Updated sort order for each rule |
