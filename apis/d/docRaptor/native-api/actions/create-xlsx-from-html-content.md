# Create XLSX from HTML Content with DocRaptor

Creates an XLSX document in DocRaptor from HTML content.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs`
- **Base URL:** `https://api.docraptor.com`
- **Official documentation:** [Create XLSX from HTML Content](https://docraptor.com/documentation/api/making_documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_content` | body | `string` | yes | HTML/XML content to convert into an XLSX spreadsheet. |
| `name` | body | `string` | no | Optional output file name. |
| `test` | body | `boolean` | no | Create a test document instead of a production document. |
