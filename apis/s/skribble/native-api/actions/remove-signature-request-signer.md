# Remove Signature Request Signer with Skribble

Removes a signer from a signature request in Skribble.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/signature-requests/:signatureRequestId/signatures/:signatureId`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Remove Signature Request Signer](https://api-doc.skribble.com/#f3170c1e-1ebe-4b52-ad25-bb4fac976f3d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureId` | path | `string` | yes | The signature ID to remove. |
| `signatureRequestId` | path | `string` | yes | The signature request ID. |
