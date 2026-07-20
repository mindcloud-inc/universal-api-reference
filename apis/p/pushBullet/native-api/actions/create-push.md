# Create Push with Pushbullet

Creates a new push in Pushbullet.

## Endpoint

- **Method:** `POST`
- **Path:** `/pushes`
- **Base URL:** `https://api.pushbullet.com/v2`
- **Official documentation:** [Create Push](https://docs.pushbullet.com/v8/#pushes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Push type (note, link, file). |
| `title` | body | `string` | no | Push title. |
| `body` | body | `string` | no | Push body content. |
| `url` | body | `string` | no | URL for link pushes. |
| `file_name` | body | `string` | no | Name of the uploaded file for file pushes. |
| `file_type` | body | `string` | no | MIME type of the uploaded file for file pushes. |
| `file_url` | body | `string` | no | Uploaded file URL returned from upload-request. |
