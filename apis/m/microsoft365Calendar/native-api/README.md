# Microsoft 365 Calendar: Native API Reference

A consolidated summary of Microsoft 365 Calendar's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/graph/api/resources/calendar?view=graph-rest-1.0
- **API base URL:** `https://graph.microsoft.com`

## Authentication

### Microsoft Entra OAuth2

Connect to Microsoft 365 Calendar through Microsoft Graph using a Microsoft Entra OAuth 2.0 app registration.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/common/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `offline_access openid profile https://graph.microsoft.com/User.Read https://graph.microsoft.com/Calendars.ReadWrite https://graph.microsoft.com/Calendars.ReadWrite.Shared`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-auth-code-flow)

## Pagination

Use `$top` in the query string to set the page size (default 25; accepted range 1–999). Use `$skiptoken` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Event](actions/accept-event.md) | `POST /v1.0/me/events/{{eventId}}/accept` | [docs](https://learn.microsoft.com/en-us/graph/api/event-accept?view=graph-rest-1.0) |
| [Create Event](actions/create-event.md) | `POST /v1.0/me/events` | [docs](https://learn.microsoft.com/en-us/graph/api/user-post-events?view=graph-rest-1.0) |
| [Delete Event](actions/delete-event.md) | `DELETE /v1.0/me/events/{{eventId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/event-delete?view=graph-rest-1.0) |
| [Get Event](actions/get-event.md) | `GET /v1.0/me/events/{{eventId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/event-get?view=graph-rest-1.0) |
| [List Calendar View](actions/list-calendar-view.md) | `GET /v1.0/me/calendarView` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-calendarview?view=graph-rest-1.0) |
| [List Calendars](actions/list-calendars.md) | `GET /v1.0/me/calendars` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-calendars?view=graph-rest-1.0) |
| [List Events](actions/list-events.md) | `GET /v1.0/me/events` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-events?view=graph-rest-1.0) |
| [Update Event](actions/update-event.md) | `PATCH /v1.0/me/events/{{eventId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/event-update?view=graph-rest-1.0) |
