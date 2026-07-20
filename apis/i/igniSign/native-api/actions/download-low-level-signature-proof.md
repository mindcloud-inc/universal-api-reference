# Download Low-Level Signature Proof with IgniSign

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/documents/:documentId/signatures/:signatureType/signers/:signerId`
- **Base URL:** `https://api.ignisign.io`
- **Official documentation:** [Download Low-Level Signature Proof](https://ignisign.io/docs/ignisign-api/documents/download-low-level-signature-proof)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The IgniSign document ID. |
| `signatureType` | path | `string` | yes | The signature type to download. |
| `signerId` | path | `string` | yes | The IgniSign signer ID. |
