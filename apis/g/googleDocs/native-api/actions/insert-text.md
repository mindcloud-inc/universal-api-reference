# Insert Text with Google Docs

Inserts text into a Google Docs document.

## Endpoint

- **Method:** `POST`
- **Path:** `/[:documentId]\:batchUpdate`
- **Base URL:** `https://docs.googleapis.com/v1/documents`
- **Official documentation:** [Insert Text](https://developers.google.com/workspace/docs/api/reference/rest/v1/documents/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `list<string>` | yes | ID of the document to update |
| `requests[0].insertText.location.index` | body | `number` | yes | Index position where text should be inserted |
| `requests[0].insertText.text` | body | `string` | yes | Text to insert |
