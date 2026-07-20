# Sign Document with SigningHub

Signs a document in SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/:packageId/documents/:documentId/sign`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Sign Document](https://manuals.nsignhub.com/latest/Api/#tag/Document-Processing/operation/V4_Signing_SignDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package containing the document to sign. |
| `documentId` | path | `number` | yes | The document to sign. |
| `field_name` | body | `string` | yes | The signature field name to sign. This field is required by the SigningHub API. |
| `hand_signature_image` | body | `string` | yes | Base64-encoded hand signature image to apply when signing. |
