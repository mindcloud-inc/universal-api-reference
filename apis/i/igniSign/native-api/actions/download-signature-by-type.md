# Download Signature by Type with IgniSign

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/documents/:documentId/signatures/:signatureType`
- **Base URL:** `https://api.ignisign.io`
- **Official documentation:** [Download Signature by Type](https://ignisign.io/docs/ignisign-api/documents/download-signature-by-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The IgniSign document ID. |
| `signatureType` | path | `string` | yes | The signature type to download. |
