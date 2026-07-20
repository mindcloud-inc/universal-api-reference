# Fetch Signature Request with Yousign

Retrieves a signature request from Yousign.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature_requests/:signatureRequestId`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [Fetch Signature Request](https://developers.yousign.com/reference/get-signature_requests-signaturerequestid-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The Yousign signature request ID. |
