# Delete Multiple Standardizations with DocuPanda - Document Understanding

Deletes existing standardizations from DocuPanda.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/standardizations`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Delete Multiple Standardizations](https://docs.docupipe.ai/reference/delete_standardizations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `standardizationIds` | body | `list<string>` | yes | List of standardization IDs to be deleted. |
| `standardizationIds[]` | body | `array<string>` | yes | List of standardization IDs to be deleted. |
