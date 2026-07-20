# Get Signature Request Files as File URL with Dropbox Sign

Retrieves signature request files as file URLs from Dropbox Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature_request/files_as_file_url/:signature_request_id`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Get Signature Request Files as File URL](https://developers.hellosign.com/api/reference/operation/signatureRequestFilesAsFileUrl/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `force_download` | query | `number` | no | Set to 0 to display the PDF in the browser instead of downloading it. |
| `signature_request_id` | path | `string` | yes | The ID of the Signature Request to retrieve files for. |
