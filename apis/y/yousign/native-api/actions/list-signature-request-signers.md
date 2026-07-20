# List Signature Request Signers with Yousign

Retrieves signers from a Yousign signature request.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature_requests/:signatureRequestId/signers`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [List Signature Request Signers](https://developers.yousign.com/reference/get-signature_requests-signaturerequestid-signers-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The Yousign signature request ID. |
