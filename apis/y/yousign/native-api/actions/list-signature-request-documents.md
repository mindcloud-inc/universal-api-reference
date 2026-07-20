# List Signature Request Documents with Yousign

Retrieves documents from a Yousign signature request.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature_requests/:signatureRequestId/documents`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [List Signature Request Documents](https://developers.yousign.com/reference/get-signature_requests-signaturerequestid-documents-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The Yousign signature request ID. |
| `nature[eq]` | query | `string` | no | Filter documents by nature. |
