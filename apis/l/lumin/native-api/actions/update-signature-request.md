# Update Signature Request with Lumin

## Endpoint

- **Method:** `PATCH`
- **Path:** `/signature_request/:signature_request_id`
- **Base URL:** `https://api.luminpdf.com/v1`
- **Official documentation:** [Update Signature Request](https://developers.luminpdf.com/api/update-signature-request/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signature_request_id` | path | `string` | yes | ID of the signature request. |
| `expires_at` | body | `number` | yes | Future Unix timestamp in milliseconds. |
