# Update Calendar with Recallai

Updates an existing calendar in Recallai.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/calendars/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Update Calendar](https://docs.recall.ai/reference/calendars_partial_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A UUID string identifying this calendar. |
| `oauth_client_id` | body | `string` | no | Oauth Client ID |
| `oauth_client_secret` | body | `string` | no | Oauth Client Secret |
| `oauth_email` | body | `string` | no | Oauth Email |
| `oauth_refresh_token` | body | `string` | no | Oauth Refresh Token |
