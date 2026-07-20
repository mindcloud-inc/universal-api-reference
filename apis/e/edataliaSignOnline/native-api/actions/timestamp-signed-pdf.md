# Timestamp Signed PDF with edatalia Sign Online

Adds a timestamp to a signed PDF in edatalia Sign Online.

## Endpoint

- **Method:** `POST`
- **Path:** `/eSign/v40/Signature/Timestamp`
- **Base URL:** `https://restapi.firmar.online`
- **Official documentation:** [Timestamp Signed PDF](https://restapi.firmar.online/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `b64PDFContent` | body | `string` | yes | Signed PDF document content encoded as base64. |
| `timestampProvider` | body | `object` | no | Optional external timestamp provider settings. |
