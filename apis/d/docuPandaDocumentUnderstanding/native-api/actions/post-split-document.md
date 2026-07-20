# Split a Document with DocuPanda - Document Understanding

Creates split documents from a DocuPanda document.

## Endpoint

- **Method:** `POST`
- **Path:** `/document/split`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Split a Document](https://docs.docupipe.ai/reference/post_split_document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | body | `string` | no | Dataset to assign to the newly generated documents. |
| `displayMode` | body | `string` | no | — |
| `documentId` | body | `string` | yes | Unique identifier of the document to be split. |
| `filenamePrefix` | body | `string` | no | Prefix to use for the filenames of the newly generated documents. |
| `instructions` | body | `string` | no | Instructions for how the splitting should be done (optional). |
