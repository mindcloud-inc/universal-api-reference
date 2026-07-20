# Update Zoom OAuth App with Recallai

Updates an existing Zoom OAuth app in Recallai.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/zoom-oauth-apps/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Update Zoom OAuth App](https://docs.recall.ai/reference/zoom_oauth_apps_partial_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_secret` | body | `string` | no | Client Secret |
| `id` | path | `string` | yes | A UUID string identifying this zoom o auth app. |
| `webhook_secret` | body | `string` | no | Webhook Secret |
