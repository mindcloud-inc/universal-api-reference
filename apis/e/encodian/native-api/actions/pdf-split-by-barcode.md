# PDF Split By Barcode with Encodian

Splits a PDF by barcode in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/SplitPdfByBarcode`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Split By Barcode](https://support.encodian.com/hc/en-gb/articles/360013629457)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filename` | body | `string` | yes | The filename of the source PDF document including the file extension. |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the source PDF document. |
| `SplitPdfByBarcodeValue` | body | `string` | no | Optionally specify a whole barcode value to match. |
| `SplitPdfByBarcodeType` | body | `string` | yes | Select whether to split on the first instance, last instance, or all instances matching the barcode value. |
| `SplitPdfByBarcodeAction` | body | `string` | yes | Select whether to split on, before, after, or remove the page containing the barcode. |
| `BarcodeReadConfidence` | body | `string` | no | Set the confidence level for barcode detection. |
| `AppendBarcodeValue` | body | `boolean` | no | Set whether to add the barcode value to the output filename. |
