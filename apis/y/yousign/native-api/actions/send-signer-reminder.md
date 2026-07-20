# Send Signer Reminder with Yousign

Sends a reminder to a Yousign signer.

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_requests/:signatureRequestId/signers/:signerId/send_reminder`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [Send Signer Reminder](https://developers.yousign.com/reference/post-signature_requests-signaturerequestid-signers-signerid-send_reminder-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The Yousign signature request ID. |
| `signerId` | path | `string` | yes | The Yousign signer ID. |
