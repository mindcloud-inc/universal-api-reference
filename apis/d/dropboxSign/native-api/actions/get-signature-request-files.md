# Get Signature Request Files with Dropbox Sign

Retrieves signature request files from Dropbox Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature_request/files/:signature_request_id`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Get Signature Request Files](https://developers.hellosign.com/api/reference/operation/signatureRequestFiles/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_type` | query | `string` | no | Set to pdf for a single merged document or zip for a collection of individual documents. |
| `signature_request_id` | path | `string` | yes | The ID of the Signature Request to retrieve files for. |
