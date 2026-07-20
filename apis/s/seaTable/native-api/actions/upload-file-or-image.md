# Upload File Or Image with SeaTable

Uploads a file or image to SeaTable.

## Endpoint

- **Method:** `POST`
- **Path:** `/seafhttp/upload-api/:upload_link?ret-json=1`
- **Base URL:** `https://cloud.seatable.io`
- **Official documentation:** [Upload File Or Image](https://api.seatable.com/reference/uploadfile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upload_link` | path | `string` | yes | The upload link returned by the upload-link bootstrap action. |
