# Get Signature Request File with Lumin

## Endpoint

- **Method:** `GET`
- **Path:** `/signature_request/:signature_request_id/file`
- **Base URL:** `https://api.luminpdf.com/v1`
- **Official documentation:** [Get Signature Request File](https://developers.luminpdf.com/api/get-signature-request-file/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signature_request_id` | path | `string` | yes | ID of the signature request. |
| `type` | query | `string` | no | Artifact to return: agreement, coc, or merged. |
