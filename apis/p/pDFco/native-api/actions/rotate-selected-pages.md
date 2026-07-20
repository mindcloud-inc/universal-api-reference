# Rotate Selected Pages with PDF.co

Rotates selected PDF pages in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/edit/rotate`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Rotate Selected Pages](https://docs.pdf.co/api-tester/pdf-rotate/basic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source PDF URL. |
| `pages` | body | `string` | yes | Pages to rotate, e.g. 1-3. |
| `angle` | body | `number` | no | Rotation angle in degrees (90, 180, 270). |
| `async` | body | `boolean` | no | Set true to run as async job. |
