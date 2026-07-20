# Create Calendar with Recallai

Creates a new calendar in Recallai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/calendars/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Create Calendar](https://docs.recall.ai/reference/calendars_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `oauth_client_id` | body | `string` | yes | Oauth Client ID |
| `oauth_client_secret` | body | `string` | yes | Oauth Client Secret |
| `oauth_email` | body | `string` | no | Oauth Email |
| `oauth_refresh_token` | body | `string` | yes | Oauth Refresh Token |
| `platform` | body | `string` | yes | * `google_calendar` - Google Calendar * `microsoft_outlook` - Microsoft Outlook |
