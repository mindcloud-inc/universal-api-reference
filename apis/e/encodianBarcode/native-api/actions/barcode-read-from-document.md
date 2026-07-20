# Barcode - Read from Document with Encodian - Barcode

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Barcodes/ReadBarcodeFromDocument`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Barcode - Read from Document](https://support.encodian.com/hc/en-gb/articles/360006170938-Read-Barcode-Document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileType` | body | `string` | yes | Source document format, such as PDF or DOCX. Accepted values: `0`, `1`, `2`. |
| `FileContent` | body | `string` | yes | Base64 source document file content. |
| `barcodeReadConfidence` | body | `string` | no | Confidence level for barcode detection. |
| `barcodeReadQuality` | body | `string` | no | Quality level for barcode detection. |
| `startPage` | body | `number` | no | Page number to begin reading from. |
| `endPage` | body | `number` | no | Page number to end reading on. |
| `barcodeRemoveControlChars` | body | `boolean` | no | Remove recognized control characters from decoded values. |
