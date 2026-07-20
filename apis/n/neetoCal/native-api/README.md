# NeetoCal: Native API Reference

A consolidated summary of NeetoCal's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.neetocal.com
- **API base URL:** `https://{subdomain}.neetocal.com/api/external/v2`

## Authentication

### API Key

Connect with a NeetoCal API key and workspace subdomain.

### Credentials

- **API Key:** `apiKey` · required
- **Subdomain:** `subdomain` · required · The workspace subdomain from your NeetoCal URL, such as acmecorp.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://neetocal-apis.mintlify.app/getting-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page_size` in the query string to set the page size (default 30; minimum 1). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Duration](actions/create-meeting-duration.md) | `POST /meetings/:meeting_sid/durations` | [docs](https://apidocs.neetocal.com/api-reference/meeting-durations/create) |
| [Create Place](actions/create-meeting-place.md) | `POST /meetings/:meeting_sid/spots` | [docs](https://apidocs.neetocal.com/api-reference/meeting-places/create) |
| [Create One-Time Scheduling Link](actions/create-one-time-scheduling-link.md) | `POST /meetings/:meeting_sid/one-off-links` | [docs](https://apidocs.neetocal.com/api-reference/scheduling-links/create-one-off) |
| [Create Scheduling Link](actions/create-scheduling-link.md) | `POST /meetings` | [docs](https://apidocs.neetocal.com/api-reference/scheduling-links/create) |
| [Delete Duration](actions/delete-meeting-duration.md) | `DELETE /meetings/:meeting_sid/durations/:id` | [docs](https://apidocs.neetocal.com/api-reference/meeting-durations/delete) |
| [Delete Place](actions/delete-meeting-place.md) | `DELETE /meetings/:meeting_sid/spots/:id` | [docs](https://apidocs.neetocal.com/api-reference/meeting-places/delete) |
| [Delete Scheduling Link](actions/delete-scheduling-link.md) | `DELETE /meetings/:meeting_sid` | [docs](https://apidocs.neetocal.com/api-reference/scheduling-links/delete) |
| [Get Duration](actions/get-meeting-duration.md) | `GET /meetings/:meeting_sid/durations/:id` | [docs](https://apidocs.neetocal.com/api-reference/meeting-durations/get) |
| [Get Place](actions/get-meeting-place.md) | `GET /meetings/:meeting_sid/spots/:id` | [docs](https://apidocs.neetocal.com/api-reference/meeting-places/get) |
| [Get Scheduling Link](actions/get-scheduling-link.md) | `GET /meetings/:meeting_sid` | [docs](https://apidocs.neetocal.com/api-reference/scheduling-links/get) |
| [Get Team Member](actions/get-team-member.md) | `GET /team-members/:team_member_id` | [docs](https://apidocs.neetocal.com/api-reference/team-members/get) |
| [List Available Slots](actions/list-available-slots.md) | `GET /meetings/:meeting_sid/slots` | [docs](https://apidocs.neetocal.com/api-reference/slots/list) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://neetocal-apis.mintlify.app/api-reference/bookings/list) |
| [List Durations for a Meeting](actions/list-meeting-durations.md) | `GET /meetings/:meeting_sid/durations` | [docs](https://apidocs.neetocal.com/api-reference/meeting-durations/list) |
| [List Places for a Meeting](actions/list-meeting-places.md) | `GET /meetings/:meeting_sid/spots` | [docs](https://apidocs.neetocal.com/api-reference/meeting-places/list) |
| [List Scheduling Links](actions/list-scheduling-links.md) | `GET /meetings` | [docs](https://apidocs.neetocal.com/api-reference/scheduling-links/list) |
| [List Team Members](actions/list-team-members.md) | `GET /team-members` | [docs](https://apidocs.neetocal.com/api-reference/team-members/list) |
| [Update Duration](actions/update-meeting-duration.md) | `PUT /meetings/:meeting_sid/durations/:id` | [docs](https://apidocs.neetocal.com/api-reference/meeting-durations/update) |
| [Update Place](actions/update-meeting-place.md) | `PUT /meetings/:meeting_sid/spots/:id` | [docs](https://apidocs.neetocal.com/api-reference/meeting-places/update) |
| [Update Scheduling Link](actions/update-scheduling-link.md) | `PATCH /meetings/:meeting_sid` | [docs](https://apidocs.neetocal.com/api-reference/scheduling-links/update) |
