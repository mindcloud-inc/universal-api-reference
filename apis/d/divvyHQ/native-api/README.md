# DivvyHQ: Native API Reference

A consolidated summary of DivvyHQ's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://developer.divvyhq.com/
- **OpenAPI specification:** https://developer.divvyhq.com/openapi.yml
- **API base URL:** `https://app.divvyhq.com/api/2.0`

## Authentication

### API Key

Use your DivvyHQ login email together with an API key generated from My Profile > API Keys.

### Credentials

- **API Key:** `apiKey` · required
- **Username Email:** `username` · required · Email address used to log into DivvyHQ. MindCloud combines this value with the API key in the Authorization header.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.lytho.com/support/solutions/articles/151000190746-my-profile-api-access)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `next`.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0. Follow the complete next-page URL returned by the API.

## Sorting

Set the sort field with `ordering` in the query string. Only one sort field is accepted.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns/` | [docs](https://developer.divvyhq.com/) |
| [Create Content Item](actions/create-content-item.md) | `POST /contentitems/` | [docs](https://developer.divvyhq.com/) |
| [Create Production Task](actions/create-production-task.md) | `POST /productiontasks/` | [docs](https://developer.divvyhq.com/) |
| [Create Simple Calendar](actions/create-simple-calendar.md) | `POST /simplecalendars/` | [docs](https://developer.divvyhq.com/) |
| [Get Base Calendar](actions/get-base-calendar.md) | `GET /basecalendars/:id/` | [docs](https://developer.divvyhq.com/) |
| [Get Calendar Entry](actions/get-calendar-entry.md) | `GET /calendarentries/:id/` | [docs](https://developer.divvyhq.com/) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:id/` | [docs](https://developer.divvyhq.com/) |
| [Get Content Item](actions/get-content-item.md) | `GET /contentitems/:id/` | [docs](https://developer.divvyhq.com/) |
| [Get My Profile](actions/get-my-profile.md) | `GET /myself/` | [docs](https://developer.divvyhq.com/) |
| [Get Parent Calendar](actions/get-parent-calendar.md) | `GET /parentcalendars/:id/` | [docs](https://developer.divvyhq.com/) |
| [Get Production Task](actions/get-production-task.md) | `GET /productiontasks/:id/` | [docs](https://developer.divvyhq.com/) |
| [Get Role In Calendar](actions/get-role-in-calendar.md) | `GET /roleincalendars/:id/` | [docs](https://developer.divvyhq.com/) |
| [Get Simple Calendar](actions/get-simple-calendar.md) | `GET /simplecalendars/:id/` | [docs](https://developer.divvyhq.com/) |
| [Get Team Member](actions/get-team-member.md) | `GET /teammembers/:id/` | [docs](https://developer.divvyhq.com/) |
| [List Allowed Content Types In Calendars](actions/list-allowed-content-types-in-calendars.md) | `GET /allowedctypeincalendars/` | [docs](https://developer.divvyhq.com/) |
| [List Base Calendars](actions/list-base-calendars.md) | `GET /basecalendars/` | [docs](https://developer.divvyhq.com/) |
| [List Calendar Entries](actions/list-calendar-entries.md) | `GET /calendarentries/` | [docs](https://developer.divvyhq.com/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns/` | [docs](https://developer.divvyhq.com/) |
| [List Content Items](actions/list-content-items.md) | `GET /contentitems/` | [docs](https://developer.divvyhq.com/) |
| [List Parent Calendars](actions/list-parent-calendars.md) | `GET /parentcalendars/` | [docs](https://developer.divvyhq.com/) |
| [List Production Tasks](actions/list-production-tasks.md) | `GET /productiontasks/` | [docs](https://developer.divvyhq.com/) |
| [List Roles In Calendars](actions/list-roles-in-calendars.md) | `GET /roleincalendars/` | [docs](https://developer.divvyhq.com/) |
| [List Team Members](actions/list-team-members.md) | `GET /teammembers/` | [docs](https://developer.divvyhq.com/) |
| [Patch Allowed Content Type In Calendar](actions/patch-allowed-content-type-in-calendar.md) | `PATCH /allowedctypeincalendars/:id/` | [docs](https://developer.divvyhq.com/) |
| [Patch Campaign](actions/patch-campaign.md) | `PATCH /campaigns/:id/` | [docs](https://developer.divvyhq.com/) |
| [Patch Content Item](actions/patch-content-item.md) | `PATCH /contentitems/:id/` | [docs](https://developer.divvyhq.com/) |
| [Patch Production Task](actions/patch-production-task.md) | `PATCH /productiontasks/:id/` | [docs](https://developer.divvyhq.com/) |
| [Patch Simple Calendar](actions/patch-simple-calendar.md) | `PATCH /simplecalendars/:id/` | [docs](https://developer.divvyhq.com/) |
| [Search Calendar Entries](actions/search-calendar-entries.md) | `POST /calendarentries/` | [docs](https://developer.divvyhq.com/) |
| [Update Campaign](actions/update-campaign.md) | `PUT /campaigns/:id/` | [docs](https://developer.divvyhq.com/) |
| [Update Content Item](actions/update-content-item.md) | `PUT /contentitems/:id/` | [docs](https://developer.divvyhq.com/) |
| [Update Production Task](actions/update-production-task.md) | `PUT /productiontasks/:id/` | [docs](https://developer.divvyhq.com/) |
| [Update Simple Calendar](actions/update-simple-calendar.md) | `PUT /simplecalendars/:id/` | [docs](https://developer.divvyhq.com/) |
