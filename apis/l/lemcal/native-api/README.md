# Lemcal: Native API Reference

A consolidated summary of Lemcal's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://developer.lemcal.com/
- **API base URL:** `https://api.lemcal.com/api/lemcal`

## Authentication

### Authorization Header

Provide the Base64-encoded Lemcal userId:apiKey value. MindCloud adds the Basic prefix in the request header.

### Credentials

- **Authorization Header:** `authorization` · required · Enter only the Base64-encoded Lemcal userId:apiKey value. Do not include the Basic prefix.

[Official authentication documentation](https://developer.lemcal.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Hook](actions/create-hook.md) | `POST /hooks` | [docs](https://developer.lemcal.com/#create-a-hook) |
| [Delete Hook](actions/delete-hook.md) | `DELETE /hooks/:id` | [docs](https://developer.lemcal.com/#delete-a-hook) |
| [Get Meeting Type](actions/get-meeting-type.md) | `GET /meetingTypes/:_id` | [docs](https://developer.lemcal.com/#get-a-meeting-type) |
| [List Booked Meetings](actions/list-booked-meetings.md) | `GET /meetings` | [docs](https://developer.lemcal.com/#list-booked-meetings) |
| [List Meeting Types](actions/list-meeting-types.md) | `GET /meetingTypes` | [docs](https://developer.lemcal.com/#list-meeting-types) |
| [Validate Authentication](actions/validate-authentication.md) | `GET /me` | [docs](https://developer.lemcal.com/#authentication) |
