# Upload Custom File with Print.one Postcards

Uploads a custom file to Print.one Postcards.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/customfiles`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Upload Custom File](https://api.print.one/docs/v2#operation/CustomFiles/uploadCustomFile)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file to upload |
