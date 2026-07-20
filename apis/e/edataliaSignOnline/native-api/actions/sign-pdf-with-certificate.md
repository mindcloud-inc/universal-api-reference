# Sign PDF With Certificate with edatalia Sign Online

Signs a PDF with a certificate in edatalia Sign Online.

## Endpoint

- **Method:** `POST`
- **Path:** `/eSign/v40/Signature`
- **Base URL:** `https://restapi.firmar.online`
- **Official documentation:** [Sign PDF With Certificate](https://restapi.firmar.online/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `b64PDFContent` | body | `string` | yes | PDF document content encoded as base64. |
| `widget` | body | `object` | yes | Signature widget definition. The API supports fixed, floating, or field-based widget shapes. |
| `certificate` | body | `object` | no | Optional signing certificate information. |
