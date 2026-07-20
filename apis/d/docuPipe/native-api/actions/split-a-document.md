# Split a Document with DocuPipe

Splits a document in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/document/split`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Split a Document](https://docs.docupipe.ai/reference/post_split_document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | body | `string` | yes | Unique identifier of the document to be split. |
| `instructions` | body | `string` | no | Instructions for how the splitting should be done (optional). |
| `dataset` | body | `string` | no | Dataset to assign to the newly generated documents. |
| `filenamePrefix` | body | `string` | no | Prefix to use for the filenames of the newly generated documents. |
| `displayMode` | body | `list` | no | *Advanced Feature* Mode of display to run. The options are: `auto`: AI decides how to display the document (default) `spatial`: Display text spatially, as it appears in the document `sections`: Display text from top to bottom as sections, with tables appearing as markdown `image`: Display as an image. Accepted values: `auto`, `image`, `sections`, `spatial`. |
