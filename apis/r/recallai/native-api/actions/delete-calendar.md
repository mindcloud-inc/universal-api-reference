# Delete Calendar with Recallai

Deletes an existing calendar from Recallai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/calendars/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Delete Calendar](https://docs.recall.ai/reference/calendars_destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A UUID string identifying this calendar. |
