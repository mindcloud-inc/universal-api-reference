# Download Signature Request Documents with Yousign

Downloads documents from a Yousign signature request.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature_requests/:signatureRequestId/documents/download`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [Download Signature Request Documents](https://developers.yousign.com/reference/get-signature_requests-signaturerequestid-documents-download-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The Yousign signature request ID. |
| `version` | query | `string` | no | Which document version to download. |
| `archive` | query | `boolean` | no | Force ZIP archive download. |
