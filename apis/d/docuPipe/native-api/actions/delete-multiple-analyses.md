# Delete Multiple Analyses with DocuPipe

Deletes multiple analyses from DocuPipe.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/analyses`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Delete Multiple Analyses](https://docs.docupipe.ai/reference/delete_analyses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `analysisIds[]` | body | `array<string>` | yes | List of analysis IDs to be deleted. |
