# Update Document with Docage

Updates an existing document in Docage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Documents/:id`
- **Base URL:** `https://api.docage.com`
- **Official documentation:** [Update Document](https://documentation.docage.com/modifier-un-document-23707652e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Content` | body | `string` | no | The updated HTML content of the document. |
| `id` | path | `string` | yes | The Docage document ID. |
| `Name` | body | `string` | no | The updated document name. |
| `Type` | body | `number` | no | The updated document type enum value. |
