# Delete Multiple Documents with DocuPanda - Document Understanding

Deletes existing documents from DocuPanda.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/documents`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Delete Multiple Documents](https://docs.docupipe.ai/reference/delete_documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds` | body | `list<string>` | yes | List of document IDs to be deleted. |
| `documentIds[]` | body | `array<string>` | yes | List of document IDs to be deleted. |
