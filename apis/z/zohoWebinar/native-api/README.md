# Zoho Webinar: Native API Reference

A consolidated summary of Zoho Webinar's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/webinar/api/authentication.html
- **API base URL:** `https://webinar.zoho.com`

## Authentication

### OAuth 2.0

### Credentials

- **Webinar Host:** `webinarHost` · optional · Zoho Webinar host for your data center. Keep the default for US (.com) or change it to your region host such as https://webinar.zoho.eu.
- **Organization ID:** `organizationId` · required · This app requires a Zoho Organization ID. Choose the organization you want to work with before connecting.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoWebinar.manageOrg.READ,ZohoWebinar.webinar.CREATE,ZohoWebinar.webinar.READ,ZohoWebinar.webinar.UPDATE,ZohoWebinar.webinar.DELETE,ZohoWebinar.user.READ,ZohoWebinar.misc.READ,ZohoWebinar.recording.READ,ZohoWebinar.recording.DELETE,ZohoWebinar.meetinguds.READ,ZohoFiles.files.READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/webinar/api/authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Register Webinar](actions/bulk-register-webinar.md) | `POST /api/v2/:organizationId/register/:webinarKey.json` | [docs](https://www.zoho.com/webinar/api/webinar-api/bulk-registration.html) |
| [Create Poll](actions/create-poll.md) | `POST /meeting/api/v2/:organizationId/poll` | [docs](https://www.zoho.com/webinar/api/polls/create.html) |
| [Create Webinar](actions/create-webinar.md) | `POST /api/v2/:organizationId/webinar.json` | [docs](https://www.zoho.com/webinar/api/webinar-api/create-a-webinar.html) |
| [Delete Poll](actions/delete-poll.md) | `DELETE /meeting/api/v2/:organizationId/poll/:pollId` | [docs](https://www.zoho.com/webinar/api/polls/delete.html) |
| [Delete Webinar](actions/delete-webinar.md) | `DELETE /api/v2/:organizationId/webinar/:webinarKey.json` | [docs](https://www.zoho.com/webinar/api/webinar-api/delete-webinar.html) |
| [Get Attendees Report](actions/get-attendees-report.md) | `GET /meeting/api/v2/:organizationId/report/attendees` | [docs](https://www.zoho.com/webinar/api/reports/attendees.html) |
| [Get Organization Details](actions/get-organization-details.md) | `GET /api/v2/user.json` | [docs](https://www.zoho.com/webinar/api/organization-id.html) |
| [Get Polls Report](actions/get-polls-report.md) | `GET /meeting/api/v2/:organizationId/report/poll` | [docs](https://www.zoho.com/webinar/api/reports/polls.html) |
| [Get Questions Report](actions/get-questions-report.md) | `GET /meeting/api/v2/:organizationId/report/questions` | [docs](https://www.zoho.com/webinar/api/reports/question.html) |
| [Get Recording](actions/get-recording.md) | `GET /api/v2/:organizationId/recordings/:webinarKey.json` | [docs](https://www.zoho.com/webinar/api/recording-api/get-specific-recording.html) |
| [Get User](actions/get-user.md) | `GET /api/v2/:organizationId/user/:userId` | [docs](https://www.zoho.com/webinar/api/user-api/get-user-details.html) |
| [Get Webinar](actions/get-webinar.md) | `GET /api/v2/:organizationId/webinar/:webinarKey.json` | [docs](https://www.zoho.com/webinar/api/webinar-api/get-webinar-details.html) |
| [Get Webinar Attendee Report](actions/get-webinar-attendee-report.md) | `GET /api/v2/:organizationId/attendee/:webinarKey.json` | [docs](https://www.zoho.com/webinar/api/webinar-api/attendee-report.html) |
| [List Languages](actions/list-languages.md) | `GET /api/v2/language` | [docs](https://www.zoho.com/webinar/api/miscellaneous-api/list-of-languages.html) |
| [List Polls](actions/list-polls.md) | `GET /meeting/api/v2/:organizationId/poll` | [docs](https://www.zoho.com/webinar/api/polls/list.html) |
| [List Recordings](actions/list-recordings.md) | `GET /api/v2/:organizationId/recordings.json` | [docs](https://www.zoho.com/webinar/api/recording-api/get-all-recordings.html) |
| [List Time Zones](actions/list-time-zones.md) | `GET /api/v2/timezone` | [docs](https://www.zoho.com/webinar/api/miscellaneous-api/list-of-time-zones.html) |
| [List Users](actions/list-users.md) | `GET /api/v2/:organizationId/user` | [docs](https://www.zoho.com/webinar/api/user-api/list-of-users.html) |
| [List Webinar Registrations](actions/list-webinar-registrations.md) | `GET /api/v2/:organizationId/registration/:webinarKey` | [docs](https://www.zoho.com/webinar/api/webinar-api/registration.html) |
| [List Webinars](actions/list-webinars.md) | `GET /api/v2/:organizationId/webinar.json` | [docs](https://www.zoho.com/webinar/api/webinar-api/list-of-webinars.html) |
| [Update Poll](actions/update-poll.md) | `PUT /meeting/api/v2/:organizationId/poll/:pollId` | [docs](https://www.zoho.com/webinar/api/polls/update.html) |
| [Update Webinar](actions/update-webinar.md) | `PUT /api/v2/:organizationId/webinar/:webinarKey.json` | [docs](https://www.zoho.com/webinar/api/webinar-api/edit-webinar.html) |
