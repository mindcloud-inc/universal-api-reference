# Embed Signing with Docubee

Creates an embedded signing session in Docubee.

## Endpoint

- **Method:** `POST`
- **Path:** `/embed`
- **Base URL:** `https://docubee.app/api/v2`
- **Official documentation:** [Embed Signing](https://docs.docubee.app/#embedded-signing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | no | The whitelisted host domain for the embedded page. |
| `processId` | body | `string` | no | The signature process ID to embed. |
| `signerId` | body | `string` | no | The signer ID or participant identifier to embed for signing. |
