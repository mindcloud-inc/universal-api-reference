# Cancel Signature Request with Yousign

Cancels a signature request in Yousign.

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_requests/:signatureRequestId/cancel`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [Cancel Signature Request](https://developers.yousign.com/reference/post-signature_requests-signaturerequestid-cancel-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The Yousign signature request ID. |
| `reason` | body | `list<string>` | yes | Cancellation reason. Accepted values: `contractualization_aborted`, `errors_in_document`, `other`. |
| `custom_note` | body | `string` | no | Optional cancellation note. |
