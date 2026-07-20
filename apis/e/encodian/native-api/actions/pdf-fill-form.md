# PDF Fill Form with Encodian

Populates a PDF form in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/FillPdfForm`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Fill Form](https://support.encodian.com/hc/en-gb/articles/360008556077)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the PDF form file to be processed. |
| `FormData` | body | `string` | yes | The JSON string used to populate the PDF form with field values. |
