# QR Code - Read from Document with Encodian - Barcode

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Barcodes/ReadQrCodeFromDocument`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [QR Code - Read from Document](https://support.encodian.com/hc/en-gb/articles/360006165437-Read-QR-Code-Document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileType` | body | `string` | yes | Source document format, such as PDF or DOCX. Accepted values: `0`, `1`, `2`. |
| `FileContent` | body | `string` | yes | Base64 source document file content. |
| `barcodeReadConfidence` | body | `string` | no | Confidence level for QR code detection. |
| `startPage` | body | `number` | no | Page number to begin reading from. |
| `endPage` | body | `number` | no | Page number to end reading on. |
| `barcodeRemoveControlChars` | body | `boolean` | no | Remove recognized control characters from decoded values. |
