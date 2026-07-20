# Merge Documents with DocuPanda - Document Understanding

Creates a merged document in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/merge`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Merge Documents](https://docs.docupipe.ai/reference/post_merge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | body | `string` | no | Dataset to assign to the newly generated document. |
| `documentIds` | body | `list<string>` | yes | List of unique identifiers of the documents to be merged. The order of IDs determines the order of documents in the merged output. Must contain at least two document IDs. |
| `filename` | body | `string` | yes | Filename of the newly generated document after merging. |
