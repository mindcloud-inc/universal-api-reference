# Activate Signature Request with Yousign

Activates a signature request in Yousign.

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_requests/:signatureRequestId/activate`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [Activate Signature Request](https://developers.yousign.com/reference/post-signature_requests-signaturerequestid-activate-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The Yousign signature request ID. |
| `sender_id` | body | `string` | no | Optional user ID to act as the sender during activation. |
