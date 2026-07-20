# Swiss QR Code - Read from Document with Encodian - Barcode

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Barcodes/ReadSwissQrCodesFromDocument`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Swiss QR Code - Read from Document](https://support.encodian.com/hc/en-gb/articles/23404516960668)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64 source document file content. |
| `barcodeReadConfidence` | body | `string` | no | Confidence level for Swiss QR detection. |
| `barcodeReadQuality` | body | `string` | no | Quality level for Swiss QR detection. |
| `pageNumbers` | body | `string` | no | Comma-separated page numbers to inspect, such as 1,3,4. |
| `barcodeRemoveControlChars` | body | `boolean` | no | Remove recognized control characters from decoded values. |
