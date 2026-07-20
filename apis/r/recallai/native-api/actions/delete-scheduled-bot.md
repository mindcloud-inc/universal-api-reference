# Delete Scheduled Bot with Recallai

Deletes a scheduled bot from Recallai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/bot/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Delete Scheduled Bot](https://docs.recall.ai/reference/bot_destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A UUID string identifying this bot. |
