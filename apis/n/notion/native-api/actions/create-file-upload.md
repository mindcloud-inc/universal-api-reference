# Create File Upload with Notion

Initiates a new file upload in Notion.

## Endpoint

- **Method:** `POST`
- **Path:** `/file_uploads`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Create File Upload](https://developers.notion.com/reference/create-a-file-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | Name of the file to upload. |
| `mode` | body | `string` | no | Upload mode: single_part or multi_part. |
| `content_type` | body | `string` | yes | MIME content type of the file. |
| `number_of_parts` | body | `number` | no | Number of upload parts for multi-part upload. |
