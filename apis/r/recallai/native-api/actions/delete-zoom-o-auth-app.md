# Delete Zoom OAuth App with Recallai

Deletes an existing Zoom OAuth app from Recallai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/zoom-oauth-apps/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Delete Zoom OAuth App](https://docs.recall.ai/reference/zoom_oauth_apps_destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A UUID string identifying this zoom o auth app. |
