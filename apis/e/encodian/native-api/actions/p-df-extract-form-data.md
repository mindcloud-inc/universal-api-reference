# PDF Extract Form Data with Encodian

Extracts PDF form data in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/GetPdfFormData`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Extract Form Data](https://support.encodian.com/hc/en-gb/articles/360035107433)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the PDF file. |
| `OperationId` | body | `string` | no | The ID of a parent operation. |
