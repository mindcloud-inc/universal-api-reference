# Get Signing Link with Lumin

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_request/:signature_request_id/signing-link`
- **Base URL:** `https://api.luminpdf.com/v1`
- **Official documentation:** [Get Signing Link](https://developers.luminpdf.com/api/get-signing-link/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signature_request_id` | path | `string` | yes | ID of the signature request. |
| `signer_email` | body | `string` | yes | Email address of the signer whose signing link should be generated. |
