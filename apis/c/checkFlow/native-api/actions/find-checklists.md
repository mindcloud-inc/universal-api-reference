# Find Checklists with CheckFlow

## Endpoint

- **Method:** `GET`
- **Path:** `/api/checklist/find`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Find Checklists](https://docs.checkflow.io/docs/api/checklists#find-checklists)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateKey` | query | `string` | yes | The key of the template the checklist is derived from. |
| `checklistName` | query | `string` | no | Full or partial checklist name to search for. |
| `tag` | query | `string` | no | Full or partial tag name to filter by. |
| `status` | query | `string` | no | Checklist status filter. Values include ALL, SCHEDULED, INPROGRESS, and COMPLETE. |
| `createIfNotExists` | query | `boolean` | no | Whether to create a checklist if no existing checklist matches the search. |
