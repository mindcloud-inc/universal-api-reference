# Create Upload Request with Pushbullet

Creates a file upload request in Pushbullet.

## Endpoint

- **Method:** `POST`
- **Path:** `/upload-request`
- **Base URL:** `https://api.pushbullet.com/v2`
- **Official documentation:** [Create Upload Request](https://docs.pushbullet.com/v8/#upload-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | yes | Name of file to upload. |
| `file_type` | body | `string` | yes | MIME type of file. |
