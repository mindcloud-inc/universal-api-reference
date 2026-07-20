# Vyte: Native API Reference

A consolidated summary of Vyte's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://developer.vyte.in/reference/
- **API base URL:** `https://api.vyte.in`

## Authentication

### API Key + Organization

Supply the Vyte organization API key and organization ID used for tenant-scoped scheduling operations.

### Credentials

- **API Key:** `apiKey` · optional · Your Vyte organization API key.
- **Organization ID:** `organizationId` · optional · Your Vyte organization ID.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://developer.vyte.in/guides/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100).

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Book Event With Team Member](actions/book-event-with-team-member.md) | `POST v2/teams/:team_id/events` | [docs](https://developer.vyte.in/reference/teams/#create-a-team-event) |
| [Cancel Event](actions/cancel-event.md) | `POST v2/events/:event_id/cancel` | [docs](https://developer.vyte.in/reference/events/#cancel-an-event) |
| [Confirm Event](actions/confirm-event.md) | `POST v2/events/:event_id/confirm` | [docs](https://developer.vyte.in/reference/events/#confirm-an-event) |
| [Create Event](actions/create-event.md) | `POST v2/events` | [docs](https://developer.vyte.in/reference/events/#create-an-event) |
| [Create Team](actions/create-team.md) | `POST v2/teams` | [docs](https://developer.vyte.in/reference/teams/#create-a-team) |
| [Create User](actions/create-user.md) | `POST v2/users` | [docs](https://developer.vyte.in/reference/users/#create-a-user) |
| [Delete Team](actions/delete-team.md) | `DELETE v2/teams/:team_id` | [docs](https://developer.vyte.in/reference/teams/#delete-a-team) |
| [Delete User Availabilities](actions/delete-user-availabilities.md) | `DELETE v2/users/:user_id/availabilities` | [docs](https://developer.vyte.in/reference/availabilities/#delete-user-availabilities) |
| [Delete User Calendar](actions/delete-user-calendar.md) | `DELETE v2/users/:user_id/calendars/:calendar_id` | [docs](https://developer.vyte.in/reference/calendars/#delete-user-calendar) |
| [List Available Slots](actions/list-available-slots.md) | `GET v2/slots` | [docs](https://developer.vyte.in/reference/slots/#list-slots) |
| [List Events](actions/list-events.md) | `GET v2/events` | [docs](https://developer.vyte.in/reference/events/#list-all-events) |
| [List Slot Days](actions/list-slot-days.md) | `GET v2/slots/days` | [docs](https://developer.vyte.in/reference/slots/#list-slots-days) |
| [List Team Available Slots](actions/list-team-available-slots.md) | `GET v2/slots` | [docs](https://developer.vyte.in/guides/setup-team-booking/#get-available-slots-for-your-team) |
| [List Team Members' Events](actions/list-team-members-events.md) | `GET v2/teams/:team_id/events` | [docs](https://developer.vyte.in/reference/teams/#list-team-events) |
| [List Team Slot Days](actions/list-team-slot-days.md) | `GET v2/slots/days` | [docs](https://developer.vyte.in/reference/slots/#list-slots-days) |
| [List Teams](actions/list-teams.md) | `GET v2/teams` | [docs](https://developer.vyte.in/reference/teams/#list-all-teams) |
| [List User Calendars](actions/list-user-calendars.md) | `GET v2/users/:user_id/calendars` | [docs](https://developer.vyte.in/reference/calendars/#list-user-calendars) |
| [List Users](actions/list-users.md) | `GET /v2/users` | [docs](https://developer.vyte.in/reference/users/#list-all-users) |
| [Remove User From Organization](actions/remove-user-from-organization.md) | `DELETE v2/users/:user_id` | [docs](https://developer.vyte.in/reference/users/#delete-a-user) |
| [Retrieve Event](actions/retrieve-event.md) | `GET v2/events/:event_id` | [docs](https://developer.vyte.in/reference/events/#retrieve-an-event) |
| [Retrieve Team](actions/retrieve-team.md) | `GET v2/teams/:team_id` | [docs](https://developer.vyte.in/reference/teams/#retrieve-a-team) |
| [Retrieve User](actions/retrieve-user.md) | `GET v2/users/:user_id` | [docs](https://developer.vyte.in/reference/users/#retrieve-a-user) |
| [Retrieve User Availabilities](actions/retrieve-user-availabilities.md) | `GET v2/users/:user_id/availabilities` | [docs](https://developer.vyte.in/reference/availabilities/#retrieve-user-availabilities) |
| [Set User Availabilities](actions/set-user-availabilities.md) | `POST v2/users/:user_id/availabilities` | [docs](https://developer.vyte.in/reference/availabilities/#create-user-availabilities) |
| [Update Event](actions/update-event.md) | `PUT v2/events/:event_id` | [docs](https://developer.vyte.in/reference/events/#update-an-event) |
| [Update Team](actions/update-team.md) | `PUT v2/teams/:team_id` | [docs](https://developer.vyte.in/reference/teams/#update-a-team) |
| [Update User](actions/update-user.md) | `PUT v2/users/:user_id` | [docs](https://developer.vyte.in/reference/users/#update-a-user) |
| [Update User Availabilities](actions/update-user-availabilities.md) | `PUT v2/users/:user_id/availabilities` | [docs](https://developer.vyte.in/reference/availabilities/#update-user-availabilities) |
| [Update User Calendars](actions/update-user-calendars.md) | `PUT v2/users/:user_id/calendars` | [docs](https://developer.vyte.in/reference/calendars/#update-user-calendars) |
