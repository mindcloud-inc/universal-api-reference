# Create Document with Lumin

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://api.luminpdf.com/v1`
- **Official documentation:** [Create Document](https://developers.luminpdf.com/api/create-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_name` | body | `string` | yes | Human-friendly title of the document. |
| `document_data.file_url` | body | `string` | yes | HTTPS URL for the source file to import into Lumin. |
