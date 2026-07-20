# Get Signature Request Files as Data URI with Dropbox Sign

Retrieves signature request files as data URIs from Dropbox Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature_request/files_as_data_uri/:signature_request_id`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Get Signature Request Files as Data URI](https://developers.hellosign.com/api/reference/operation/signatureRequestFilesAsDataUri/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signature_request_id` | path | `string` | yes | The ID of the Signature Request to retrieve files for. |
