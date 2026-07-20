# Zoho Calendar: Native API Reference

A consolidated summary of Zoho Calendar's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/calendar/help/api/introduction.html
- **API base URL:** `https://calendar.zoho.com/api/v1`

## Authentication

### OAuth 2.0

Connect Zoho Calendar with OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoCalendar.group.READ,ZohoCalendar.calendar.READ,ZohoCalendar.calendar.CREATE,ZohoCalendar.calendar.UPDATE,ZohoCalendar.calendar.DELETE,ZohoCalendar.event.READ,ZohoCalendar.event.CREATE,ZohoCalendar.event.UPDATE,ZohoCalendar.event.DELETE,ZohoCalendar.settings.READ,ZohoCalendar.settings.UPDATE,ZohoCalendar.notification.READ,ZohoCalendar.notification.UPDATE,ZohoCalendar.search.READ,ZohoCalendar.freebusy.READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/calendar/help/api/oauth2-user-guide.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Calendar](actions/create-calendar.md) | `POST /calendars` | [docs](https://www.zoho.com/calendar/help/api/post-create-calendar.html) |
| [Create Event](actions/create-event.md) | `POST /calendars/:calendaruid/events` | [docs](https://www.zoho.com/calendar/help/api/post-create-event.html) |
| [Create Event Using Smart Add](actions/create-event-using-smart-add.md) | `POST /smartadd` | [docs](https://www.zoho.com/calendar/help/api/post-create-event-smart-add.html) |
| [Delete Calendar](actions/delete-calendar.md) | `DELETE /calendars/:calendaruid` | [docs](https://www.zoho.com/calendar/help/api/delete-calendar.html) |
| [Delete Event](actions/delete-event.md) | `DELETE /calendars/:calendaruid/events/:eventuid` | [docs](https://www.zoho.com/calendar/help/api/delete-event.html) |
| [Get Calendar Details](actions/get-calendar-details.md) | `GET /calendars/:calendaruid` | [docs](https://www.zoho.com/calendar/help/api/get-calendar-details.html) |
| [Get Calendar Settings](actions/get-calendar-settings.md) | `GET /settings` | [docs](https://www.zoho.com/calendar/help/api/get-calendar-settings.html) |
| [Get Event By Instance](actions/get-event-by-instance.md) | `GET /calendars/:calendaruid/events/:eventuid/byinstance` | [docs](https://www.zoho.com/calendar/help/api/get-event-by-instance.html) |
| [Get Event Details](actions/get-event-details.md) | `GET /calendars/:calendaruid/events/:eventuid` | [docs](https://www.zoho.com/calendar/help/api/get-event-details.html) |
| [Get Group Attendees Details](actions/get-group-attendees-details.md) | `GET /calendars/:calendaruid/events/:eventuid/groupattendeestatus` | [docs](https://www.zoho.com/calendar/help/api/get-group-attendees-details.html) |
| [Get Notification Details](actions/get-notification-details.md) | `GET /notification` | [docs](https://www.zoho.com/calendar/help/api/get-notification-details.html) |
| [Get Shared Calendar Details](actions/get-shared-calendar-details.md) | `GET /calendars/:calendaruid/share` | [docs](https://www.zoho.com/calendar/help/api/get-shared-calendar-details.html) |
| [Get User Free Busy Details](actions/get-user-free-busy-details.md) | `GET /calendars/freebusy` | [docs](https://www.zoho.com/calendar/help/api/get-user-freebusy-details.html) |
| [List Calendars](actions/list-calendars.md) | `GET /calendars` | [docs](https://www.zoho.com/calendar/help/api/get-calendar-list.html) |
| [List Events](actions/list-events.md) | `GET /calendars/:calendaruid/events` | [docs](https://www.zoho.com/calendar/help/api/get-events-list.html) |
| [List Group Calendars](actions/list-group-calendars.md) | `GET /groups` | [docs](https://www.zoho.com/calendar/help/api/get-group-calendar-list.html) |
| [Move Event](actions/move-event.md) | `POST /calendars/:calendaruid/events/:eventuid` | [docs](https://www.zoho.com/calendar/help/api/move-event.html) |
| [Partial Update Event](actions/partial-update-event.md) | `PATCH /calendars/:calendaruid/events/:eventuid` | [docs](https://www.zoho.com/calendar/help/api/patch-partial-update-event.html) |
| [Search Events](actions/search-events.md) | `GET /calendars/:calendaruid/search` | [docs](https://www.zoho.com/calendar/help/api/get-event-through-search.html) |
| [Share Calendar](actions/share-calendar.md) | `PUT /calendars/:calendaruid/share` | [docs](https://www.zoho.com/calendar/help/api/put-share-calendar.html) |
| [Update Calendar](actions/update-calendar.md) | `PUT /calendars/:calendaruid` | [docs](https://www.zoho.com/calendar/help/api/put-update-calendar.html) |
| [Update Calendar Settings](actions/update-calendar-settings.md) | `PUT /settings` | [docs](https://www.zoho.com/calendar/help/api/put-update-calendar-settings.html) |
| [Update Event](actions/update-event.md) | `PUT /calendars/:calendaruid/events/:eventuid` | [docs](https://www.zoho.com/calendar/help/api/put-update-event.html) |
| [Update Notification Details](actions/update-notification-details.md) | `PUT /notification` | [docs](https://www.zoho.com/calendar/help/api/put-update-notification-details.html) |
