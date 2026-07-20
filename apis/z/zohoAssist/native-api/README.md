# Zoho Assist: Native API Reference

A consolidated summary of Zoho Assist's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/assist/api/introduction.html
- **API base URL:** `https://assist.zoho.com/api/v2`

## Authentication

### OAuth 2.0

Zoho Accounts OAuth 2.0 for Zoho Assist.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoAssist.userapi.READ ZohoAssist.sessionapi.CREATE ZohoAssist.reportapi.READ ZohoAssist.unattended.computer.READ ZohoAssist.unattended.computer.UPDATE ZohoAssist.unattended.computer.DELETE ZohoAssist.unattended.group.READ ZohoAssist.unattended.group.CREATE ZohoAssist.unattended.group.UPDATE ZohoAssist.unattended.group.DELETE ZohoAssist.unattended.device.CREATE`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/assist/api/authentication.html)

## Pagination

Use `count` in the query string to set the page size (default 25; accepted range 1–50). Use `index` in the query string to choose the page; numbering starts at 1.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | `POST /session` | [docs](https://www.zoho.com/assist/api/createasession.html) |
| [Create Unattended Group](actions/create-unattended-group.md) | `POST /unattended_computer/group` | [docs](https://www.zoho.com/assist/api/createunattendedgroup.html) |
| [Create Unattended Session](actions/create-unattended-session.md) | `POST /unattended/:resourceId/connect` | [docs](https://www.zoho.com/assist/api/unattendedsession.html) |
| [Delete Unattended Computer](actions/delete-unattended-computer.md) | `DELETE /devices/:resourceId` | [docs](https://www.zoho.com/assist/api/deleteunattendedcomputer.html) |
| [Delete Unattended Group](actions/delete-unattended-group.md) | `DELETE /unattended_computer/group` | [docs](https://www.zoho.com/assist/api/deleteunattendedgroup.html) |
| [Get Device Details](actions/get-device-details.md) | `GET /devices/:resourceId` | [docs](https://www.zoho.com/assist/api/getDeviceDetails.html) |
| [Get User Info](actions/get-user-info.md) | `GET /user` | [docs](https://www.zoho.com/assist/api/getuserinfo.html) |
| [List Session Reports](actions/list-session-reports.md) | `GET /reports` | [docs](https://www.zoho.com/assist/api/getsessionreports.html) |
| [List Unattended Computers](actions/list-unattended-computers.md) | `GET /devices` | [docs](https://www.zoho.com/assist/api/getunattendedcomputer.html) |
| [List Unattended Groups](actions/list-unattended-groups.md) | `GET /unattended_computer/group` | [docs](https://www.zoho.com/assist/api/getunattendedgroup.html) |
| [Schedule Session](actions/schedule-session.md) | `POST /session/schedule` | [docs](https://www.zoho.com/assist/api/schedulesession.html) |
| [Update Unattended Computer](actions/update-unattended-computer.md) | `PUT /devices/:resourceId` | [docs](https://www.zoho.com/assist/api/updateunattendedcomputer.html) |
| [Update Unattended Group](actions/update-unattended-group.md) | `PUT /unattended_computer/group` | [docs](https://www.zoho.com/assist/api/updateunattendedgroup.html) |
