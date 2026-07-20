# Delete Multiple Documents with DocuPipe

Deletes multiple documents from DocuPipe.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/documents`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Delete Multiple Documents](https://docs.docupipe.ai/reference/delete_documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds[]` | body | `array<string>` | yes | List of document IDs to be deleted. |
