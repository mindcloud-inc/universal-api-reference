# Get Signature Request with Dropbox Sign

Retrieves a signature request from Dropbox Sign by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature_request/:signature_request_id`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Get Signature Request](https://developers.hellosign.com/api/reference/operation/signatureRequestGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signature_request_id` | path | `string` | yes | The id of the SignatureRequest to retrieve. |
