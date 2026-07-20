# PDF Flatten with Encodian

Flattens a PDF document in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/FlattenPdf`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Flatten](https://support.encodian.com/hc/en-gb/articles/4416473033105)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the PDF file to be processed. |
