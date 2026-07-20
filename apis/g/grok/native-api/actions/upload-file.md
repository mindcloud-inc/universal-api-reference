# Upload File with Grok

Uploads a new file to Grok.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/files`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Upload File](https://docs.x.ai/developers/rest-api-reference/files/upload#upload-a-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File content to upload. |
| `purpose` | body | `string` | yes | Intended file purpose. |
