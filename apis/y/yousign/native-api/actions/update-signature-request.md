# Update Signature Request with Yousign

Updates an existing signature request in Yousign.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/signature_requests/:signatureRequestId`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [Update Signature Request](https://developers.yousign.com/reference/patch-signature_requests-signaturerequestid-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The Yousign signature request ID. |
| `name` | body | `string` | no | Updated signature request name. |
| `delivery_mode` | body | `string` | no | Updated delivery mode. |
| `timezone` | body | `string` | no | Updated timezone. |
| `expiration_date` | body | `string` | no | Updated due date in yyyy-mm-dd format. |
| `external_id` | body | `string` | no | Updated external ID. |
