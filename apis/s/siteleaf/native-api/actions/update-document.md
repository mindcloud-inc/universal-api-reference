# Update Document with Siteleaf

Updates an existing document in Siteleaf.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:document_id`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [Update Document](https://learn.siteleaf.com/api/documents/#update-a-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | no | Siteleaf document identifier |
| `title` | body | `string` | no | Updated document title |
