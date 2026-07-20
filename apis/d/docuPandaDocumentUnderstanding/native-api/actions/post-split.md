# Split a Document with DocuPanda - Document Understanding

Creates split documents from a DocuPanda document.

## Endpoint

- **Method:** `POST`
- **Path:** `/split`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Split a Document](https://docs.docupipe.ai/openapi/docupanda.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | body | `string` | yes | Unique identifier of the document to be split. |
| `instructions` | body | `string` | no | Instructions for how the splitting should be done (optional). |
