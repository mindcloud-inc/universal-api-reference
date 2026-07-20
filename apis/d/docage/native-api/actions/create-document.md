# Create Document with Docage

Creates a new document in Docage.

## Endpoint

- **Method:** `POST`
- **Path:** `/Documents`
- **Base URL:** `https://api.docage.com`
- **Official documentation:** [Create Document](https://documentation.docage.com/cr%C3%A9er-un-document-23707655e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Content` | body | `string` | yes | The HTML content of the document. |
| `Name` | body | `string` | yes | The document name. |
| `Type` | body | `number` | yes | The document type enum value. |
