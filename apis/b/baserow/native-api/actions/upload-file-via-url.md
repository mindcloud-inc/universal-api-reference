# Upload File Via URL with Baserow

Uploads a file to Baserow from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/user-files/upload-via-url/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [Upload File Via URL](https://api.baserow.io/api/redoc/#operation/upload_via_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The public file URL that Baserow should download and upload. |
