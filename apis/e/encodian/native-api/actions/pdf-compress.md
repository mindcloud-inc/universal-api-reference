# PDF Compress with Encodian

Compresses a PDF document in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/CompressPdf`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Compress](https://support.encodian.com/hc/en-gb/articles/360019994857-Compress-PDF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the PDF file to be processed. |
