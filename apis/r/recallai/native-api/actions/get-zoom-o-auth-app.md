# Get Zoom OAuth App with Recallai

Retrieves a Zoom OAuth app from Recallai.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/zoom-oauth-apps/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Get Zoom OAuth App](https://docs.recall.ai/reference/zoom_oauth_apps_retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A UUID string identifying this zoom o auth app. |
