# Get Checklist Details with CheckFlow

## Endpoint

- **Method:** `GET`
- **Path:** `/api/checklist/details`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Get Checklist Details](https://docs.checkflow.io/docs/api/checklists#get-checklist-details)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateKey` | query | `string` | yes | The key of the template the checklist is derived from. |
| `checklistKey` | query | `string` | no | The key of the checklist to return. |
| `checklistName` | query | `string` | no | Full or partial checklist name to search for. |
| `tag` | query | `string` | no | Full or partial tag name to filter by. |
| `status` | query | `string` | no | Checklist status filter. Values include ALL, SCHEDULED, INPROGRESS, and COMPLETE. |
