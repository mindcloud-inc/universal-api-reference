# Create Data Route with Formstack Documents

Creates a new data route in Formstack Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/routes`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Create Data Route](https://www.webmerge.me/developers/routes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder` | body | `string` | no | Folder name to save the data route in |
| `name` | body | `string` | yes | Name of the data route |
| `output_name` | body | `string` | no | Custom filename for the combined PDF output |
| `rules[][combine]` | body | `string` | no | Whether to include each rule in the combined PDF |
| `rules[][document_id]` | body | `string` | no | Document ID for each data route rule |
| `rules[][file]` | body | `string` | no | Remote file URL or merge field for each rule |
| `rules[][loop_field]` | body | `string` | no | Array field used to repeat a rule |
| `rules[][sort]` | body | `string` | no | Sort order for each rule |
