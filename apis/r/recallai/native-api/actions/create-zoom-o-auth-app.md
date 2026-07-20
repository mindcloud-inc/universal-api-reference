# Create Zoom OAuth App with Recallai

Creates a new Zoom OAuth app in Recallai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/zoom-oauth-apps/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Create Zoom OAuth App](https://docs.recall.ai/reference/zoom_oauth_apps_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | yes | Client ID |
| `client_secret` | body | `string` | yes | Client Secret |
| `kind` | body | `string` | yes | * `user_level` - User Level * `account_level` - Account Level |
| `webhook_secret` | body | `string` | yes | Webhook Secret |
