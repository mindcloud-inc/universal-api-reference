# Recallai: Native API Reference

A consolidated summary of Recallai's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://docs.recall.ai/docs/getting-started
- **API base URL:** `https://{workspaceRegion}.recall.ai`

## Authentication

### API Key

Connect Recall.ai with your workspace API key and region.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace Region:** `workspaceRegion` · required · Recall.ai workspace region slug, for example us-west-2

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.recall.ai/docs/regions)

## Pagination

Use `cursor` in the query string as the pagination cursor.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | `POST /api/v1/bot/` | [docs](https://docs.recall.ai/reference/bot_create) |
| [Create Calendar](actions/create-calendar.md) | `POST /api/v2/calendars/` | [docs](https://docs.recall.ai/reference/calendars_create) |
| [Create Desktop SDK Upload](actions/create-desktop-sdk-upload.md) | `POST /api/v1/sdk_upload/` | [docs](https://docs.recall.ai/reference/sdk_upload_create) |
| [Create Google Login](actions/create-google-login.md) | `POST /api/v2/google-logins/` | [docs](https://docs.recall.ai/reference/google_logins_create) |
| [Create Google Login Group](actions/create-google-login-group.md) | `POST /api/v2/google-login-groups/` | [docs](https://docs.recall.ai/reference/google_login_groups_create) |
| [Create Zoom OAuth App](actions/create-zoom-o-auth-app.md) | `POST /api/v2/zoom-oauth-apps/` | [docs](https://docs.recall.ai/reference/zoom_oauth_apps_create) |
| [Delete Calendar](actions/delete-calendar.md) | `DELETE /api/v2/calendars/:id/` | [docs](https://docs.recall.ai/reference/calendars_destroy) |
| [Delete Google Login](actions/delete-google-login.md) | `DELETE /api/v2/google-logins/:id/` | [docs](https://docs.recall.ai/reference/google_logins_destroy) |
| [Delete Google Login Group](actions/delete-google-login-group.md) | `DELETE /api/v2/google-login-groups/:id/` | [docs](https://docs.recall.ai/reference/google_login_groups_destroy) |
| [Delete Scheduled Bot](actions/delete-scheduled-bot.md) | `DELETE /api/v1/bot/:id/` | [docs](https://docs.recall.ai/reference/bot_destroy) |
| [Delete Zoom OAuth App](actions/delete-zoom-o-auth-app.md) | `DELETE /api/v2/zoom-oauth-apps/:id/` | [docs](https://docs.recall.ai/reference/zoom_oauth_apps_destroy) |
| [Get Bot](actions/get-bot.md) | `GET /api/v1/bot/:id/` | [docs](https://docs.recall.ai/reference/bot_retrieve) |
| [Get Calendar](actions/get-calendar.md) | `GET /api/v2/calendars/:id/` | [docs](https://docs.recall.ai/reference/calendars_retrieve) |
| [Get Desktop SDK Upload](actions/get-desktop-sdk-upload.md) | `GET /api/v1/sdk_upload/:id/` | [docs](https://docs.recall.ai/reference/sdk_upload_retrieve) |
| [Get Google Login](actions/get-google-login.md) | `GET /api/v2/google-logins/:id/` | [docs](https://docs.recall.ai/reference/google_logins_retrieve) |
| [Get Google Login Group](actions/get-google-login-group.md) | `GET /api/v2/google-login-groups/:id/` | [docs](https://docs.recall.ai/reference/google_login_groups_retrieve) |
| [Get Usage](actions/get-usage.md) | `GET /api/v1/billing/usage/` | [docs](https://docs.recall.ai/reference/billing_usage_retrieve) |
| [Get Zoom OAuth App](actions/get-zoom-o-auth-app.md) | `GET /api/v2/zoom-oauth-apps/:id/` | [docs](https://docs.recall.ai/reference/zoom_oauth_apps_retrieve) |
| [List Bot Screenshots](actions/list-bot-screenshots.md) | `GET /api/v1/bot/:bot_id/screenshots/` | [docs](https://docs.recall.ai/reference/bot_screenshots_list) |
| [List Bots](actions/list-bots.md) | `GET /api/v1/bot/` | [docs](https://docs.recall.ai/reference/bot_list) |
| [List Calendar Events](actions/list-calendar-events.md) | `GET /api/v2/calendar-events/` | [docs](https://docs.recall.ai/reference/calendar_events_list) |
| [List Calendars](actions/list-calendars.md) | `GET /api/v2/calendars/` | [docs](https://docs.recall.ai/reference/calendars_list) |
| [List Desktop SDK Uploads](actions/list-desktop-sdk-uploads.md) | `GET /api/v1/sdk_upload/` | [docs](https://docs.recall.ai/reference/sdk_upload_list) |
| [List Google Login Groups](actions/list-google-login-groups.md) | `GET /api/v2/google-login-groups/` | [docs](https://docs.recall.ai/reference/google_login_groups_list) |
| [List Google Logins](actions/list-google-logins.md) | `GET /api/v2/google-logins/` | [docs](https://docs.recall.ai/reference/google_logins_list) |
| [List Recordings](actions/list-recordings.md) | `GET /api/v1/recording/` | [docs](https://docs.recall.ai/reference/recording_list) |
| [List Zoom OAuth Apps](actions/list-zoom-o-auth-apps.md) | `GET /api/v2/zoom-oauth-apps/` | [docs](https://docs.recall.ai/reference/zoom_oauth_apps_list) |
| [Update Calendar](actions/update-calendar.md) | `PATCH /api/v2/calendars/:id/` | [docs](https://docs.recall.ai/reference/calendars_partial_update) |
| [Update Google Login](actions/update-google-login.md) | `PATCH /api/v2/google-logins/:id/` | [docs](https://docs.recall.ai/reference/google_logins_partial_update) |
| [Update Google Login Group](actions/update-google-login-group.md) | `PATCH /api/v2/google-login-groups/:id/` | [docs](https://docs.recall.ai/reference/google_login_groups_partial_update) |
| [Update Scheduled Bot](actions/update-scheduled-bot.md) | `PATCH /api/v1/bot/:id/` | [docs](https://docs.recall.ai/reference/bot_partial_update) |
| [Update Zoom OAuth App](actions/update-zoom-o-auth-app.md) | `PATCH /api/v2/zoom-oauth-apps/:id/` | [docs](https://docs.recall.ai/reference/zoom_oauth_apps_partial_update) |
