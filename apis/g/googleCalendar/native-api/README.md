# Google Calendar: Native API Reference

A consolidated summary of Google Calendar's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/workspace/calendar/api/v3/reference
- **API base URL:** `https://www.googleapis.com/calendar/v3`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/calendar.app.created https://www.googleapis.com/auth/calendar.calendarlist.readonly https://www.googleapis.com/auth/calendar.events.freebusy https://www.googleapis.com/auth/calendar.events.public.readonly https://www.googleapis.com/auth/calendar.readonly https://www.googleapis.com/auth/calendar.events https://www.googleapis.com/auth/calendar.events.owned https://www.googleapis.com/auth/calendar.events.owned.readonly https://www.googleapis.com/auth/calendar.events.readonly https://www.googleapis.com/auth/calendar https://www.googleapis.com/auth/calendar.calendarlist`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

The next-page cursor is read from `nextPageToken`.

## Pagination

Use `maxResults` in the query string to set the page size (default 100; accepted range 1–250). Use `pageToken` in the query string as the pagination cursor.

## Sorting

Set the sort field with `orderBy` in the query string. Only one sort field is accepted.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Calendar to List](actions/add-calendar-to-list.md) | `POST users/me/calendarList` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/calendarList/insert) |
| [Clear Calendar](actions/clear-calendar.md) | `POST calendars/:calendar/clear` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/calendars/clear) |
| [Create ACL Rule](actions/create-acl-rule.md) | `POST calendars/:calendar/acl` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/acl/insert) |
| [Create Calendar](actions/create-calendar.md) | `POST calendars` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/calendars/insert) |
| [Create Event](actions/create-event.md) | `POST calendars/:calendar/events` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/events/insert) |
| [Delete ACL Rule](actions/delete-acl-rule.md) | `DELETE calendars/:calendar/acl/:ruleId` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/acl/delete) |
| [Delete Event](actions/delete-event.md) | `DELETE calendars/:calendar/events/:eventId` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/events/delete) |
| [Get ACL Rule](actions/get-acl-rule.md) | `GET calendars/:calendar/acl/:ruleId` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/acl/get) |
| [Get Calendar List Entry](actions/get-calendar-list-entry.md) | `GET users/me/calendarList/:calendar` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/calendarList/get) |
| [Get Calendar Metadata](actions/get-calendar-metadata.md) | `GET calendars/:calendar` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/calendars/get) |
| [Get Colors](actions/get-colors.md) | `GET colors` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/colors/get) |
| [Get Event](actions/get-event.md) | `GET calendars/:calendar/events/:eventId` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/events/get) |
| [Get Setting](actions/get-setting.md) | `GET users/me/settings/:setting` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/settings/get) |
| [Import Event](actions/import-event.md) | `POST calendars/:calendar/events/import` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/events/import) |
| [List ACL Rules](actions/list-acl-rules.md) | `GET calendars/:calendar/acl` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/acl/list) |
| [List Calendars](actions/list-calendars.md) | `GET users/me/calendarList` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/calendarList/list) |
| [List Event Instances](actions/list-event-instances.md) | `GET calendars/:calendar/events/:eventId/instances` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/events/instances) |
| [List Events](actions/list-events.md) | `GET calendars/:calendar/events` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/events/list) |
| [List Settings](actions/list-settings.md) | `GET users/me/settings` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/settings/list) |
| [Move Event](actions/move-event.md) | `POST calendars/:calendar/events/:eventId/move` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/events/move) |
| [Patch Calendar List Entry](actions/patch-calendar-list-entry.md) | `PATCH users/me/calendarList/:calendar` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/calendarList/patch) |
| [Query Free/Busy](actions/query-free-busy.md) | `POST freeBusy` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/freebusy/query) |
| [Quick Add Event](actions/quick-add-event.md) | `POST calendars/:calendar/events/quickAdd` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/events/quickAdd) |
| [Remove Calendar from List](actions/remove-calendar-from-list.md) | `DELETE users/me/calendarList/:calendar` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/calendarList/delete) |
| [Update ACL Rule](actions/update-acl-rule.md) | `PATCH calendars/:calendar/acl/:ruleId` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/acl/patch) |
| [Update Calendar List Entry](actions/update-calendar-list-entry.md) | `PUT users/me/calendarList/:calendar` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/calendarList/update) |
| [Update Event](actions/update-event.md) | `PATCH calendars/:calendar/events/:eventId` | [docs](https://developers.google.com/workspace/calendar/api/v3/reference/events/patch) |
