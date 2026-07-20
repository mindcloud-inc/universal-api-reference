# Send Signature Request with Lumin

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_request/send`
- **Base URL:** `https://api.luminpdf.com/v1`
- **Official documentation:** [Send Signature Request](https://developers.luminpdf.com/api/send-signature-request/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_url` | body | `string` | yes | URL of the file to download and send for signature. |
| `title` | body | `string` | yes | Title of the signature request. |
| `signers[]` | body | `array<object>` | yes | Array of signer objects with email_address and name, plus group when using ORDER signing. |
| `expires_at` | body | `number` | yes | Future Unix timestamp in milliseconds when the request expires. |
| `signing_type` | body | `string` | no | Signing order. SAME_TIME or ORDER. |
