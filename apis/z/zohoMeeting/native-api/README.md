# Zoho Meeting: Native API Reference

A consolidated summary of Zoho Meeting's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/meeting/api-integration.html
- **API base URL:** `https://meeting.zoho.com`

## Authentication

### OAuth 2.0

Zoho Meeting pricing currently lists API access on the Professional plan. After OAuth succeeds, run Get Current User Details to capture the zsoid/orgId used by most Meeting and Webinar actions.

### Credentials

- **Organization ID:** `organizationId` · optional · Optional default Zoho Meeting organization ID (zsoid/orgId). Run Get Current User Details after connecting, then save the value you use most often.
- **Accounts Server URL:** `accountsServerUrl` · optional · Zoho Accounts server URL for your data center. Use the default https://accounts.zoho.com unless your Zoho account authenticates against another regional Accounts host.
- **Meeting Host:** `meetingHost` · required · Zoho Meeting host for your data center, such as meeting.zoho.com or meeting.zoho.eu. Check the browser URL after you sign in to Zoho Meeting if you are unsure.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoMeeting.manageOrg.READ,ZohoMeeting.license.READ,ZohoMeeting.user.READ,ZohoMeeting.meeting.ALL,ZohoMeeting.webinar.ALL,ZohoWebinar.webinar.READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/meeting/api-integration/authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `count` in the query string to set the page size (default 20; minimum 1). Use `index` in the query string to choose the page; numbering starts at 0.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Meeting](actions/create-meeting.md) | `POST /api/v2/:organizationId/sessions.json` | [docs](https://www.zoho.com/meeting/api-integration/meeting-api/create-a-meeting.html) |
| [Create Webinar](actions/create-webinar.md) | `POST /api/v2/:organizationId/webinar.json` | [docs](https://www.zoho.com/meeting/api-integration/webinar-api/create-a-webinar.html) |
| [Create Webinar Registrations](actions/create-webinar-registrations.md) | `POST /api/v2/:organizationId/register/:webinarKey.json` | [docs](https://www.zoho.com/meeting/api-integration/webinar-api/bulk-registration-api.html) |
| [Delete Meeting](actions/delete-meeting.md) | `DELETE /api/v2/:organizationId/sessions/:meetingKey.json` | [docs](https://www.zoho.com/meeting/api-integration/meeting-api/delete-meeting-api.html) |
| [Delete Webinar](actions/delete-webinar.md) | `DELETE /api/v2/:organizationId/webinar/:webinarKey.json` | [docs](https://www.zoho.com/meeting/api-integration/webinar-api/delete-webinar-api.html) |
| [Get Current License Details](actions/get-current-license-details.md) | `GET /api/v2/:organizationId/license` | [docs](https://www.zoho.com/meeting/api-integration/license-api/get-license-details.html) |
| [Get Current User Details](actions/get-current-user-details.md) | `GET /api/v2/user.json` | [docs](https://www.zoho.com/meeting/api-integration/organization-id.html) |
| [Get Meeting Details](actions/get-meeting-details.md) | `GET /api/v2/:organizationId/sessions/:meetingKey.json` | [docs](https://www.zoho.com/meeting/api-integration/meeting-api/get-meeting-api.html) |
| [Get User Details](actions/get-user-details.md) | `GET /api/v2/:organizationId/user/:userId` | [docs](https://www.zoho.com/meeting/api-integration/user-api/get-user-details.html) |
| [Get Webinar Details](actions/get-webinar-details.md) | `GET /api/v2/:organizationId/webinar/:webinarKey.json` | [docs](https://www.zoho.com/meeting/api-integration/webinar-api/get-webinar-api.html) |
| [List Meetings](actions/list-meetings.md) | `GET /api/v2/:organizationId/sessions.json` | [docs](https://www.zoho.com/meeting/api-integration/meeting-api/list-of-meeting-api.html) |
| [List Users](actions/list-users.md) | `GET /api/v2/:organizationId/user` | [docs](https://www.zoho.com/meeting/api-integration/user-api/list-of-users.html) |
| [List Webinar Registrations](actions/list-webinar-registrations.md) | `GET /api/v2/:organizationId/registration/:webinarKey` | [docs](https://www.zoho.com/meeting/api-integration/webinar-api/registration.html) |
| [List Webinars](actions/list-webinars.md) | `GET /api/v2/:organizationId/webinar.json` | [docs](https://www.zoho.com/meeting/api-integration/webinar-api/list-of-webinar-api.html) |
| [Update Meeting](actions/update-meeting.md) | `PUT /api/v2/:organizationId/sessions/:meetingKey.json` | [docs](https://www.zoho.com/meeting/api-integration/meeting-api/edit-meeting-api.html) |
| [Update Webinar](actions/update-webinar.md) | `PUT /api/v2/:organizationId/webinar/:webinarKey.json` | [docs](https://www.zoho.com/meeting/api-integration/webinar-api/edit-webinar.html) |
