# TimeRex: Native API Reference

A consolidated summary of TimeRex's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://developers.timerex.net/api/reference/
- **API base URL:** `https://timerex.net/api/beta`

## Authentication

### OAuth

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://timerex.net/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://timerex.net/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `profile email User.Teams.Read User.Teams.Calendars.Read User.Teams.Calendars.ReadWrite`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://timerex.net/oauth/token.

[Official authentication documentation](https://developers.timerex.net/api/reference/9554452833417-o-auth)

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Calendar](actions/get-calendar.md) | `GET /calendars/:calendarId` | [docs](https://developers.timerex.net/api/reference/) |
| [Get One Time URL](actions/get-one-time-url.md) | `GET /calendars/one-time-url/:oneTimeUrlId` | [docs](https://developers.timerex.net/api/reference/) |
| [Get Team](actions/get-team.md) | `GET /teams/:teamId` | [docs](https://developers.timerex.net/api/reference/) |
| [Get User Information](actions/get-user-information.md) | `GET /user/me` | [docs](https://developers.timerex.net/api/reference/5eeff576252d2-get-user-information) |
| [Get User Primary Team](actions/get-user-primary-team.md) | `GET /user/me/teams/primary` | [docs](https://developers.timerex.net/api/reference/) |
| [List Team Calendars](actions/list-team-calendars.md) | `GET /teams/:teamId/calendars` | [docs](https://developers.timerex.net/api/reference/) |
| [List User Teams](actions/list-user-teams.md) | `GET /user/me/teams` | [docs](https://developers.timerex.net/api/reference/) |
