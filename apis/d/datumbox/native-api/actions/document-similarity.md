# Document Similarity with Datumbox

Compares two documents for similarity in Datumbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/DocumentSimilarity.json`
- **Base URL:** `http://api.datumbox.com/1.0`
- **Official documentation:** [Document Similarity](https://www.datumbox.com/files/API-Documentation-1.0v.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `original` | body | `string` | yes | The first clear-text document to compare. |
| `copy` | body | `string` | yes | The second clear-text document to compare. |
