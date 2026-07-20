# Remove Metadata from PDF with XSS PDF Solutions

Creates a PDF without metadata in XSS PDF Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/40`
- **Base URL:** `https://api.xss-cross-service-solutions.com/solutions/solutions`
- **Official documentation:** [Remove Metadata from PDF](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#remove-metadata-from-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The PDF file from which metadata will be removed. |
