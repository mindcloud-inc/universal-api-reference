# Strava: Native API Reference

A consolidated summary of Strava's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://developers.strava.com/docs/reference/
- **API base URL:** `https://www.strava.com/api/v3`

## Authentication

### OAuth2

Strava OAuth 2.0 authorization code flow for athlete access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.strava.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://www.strava.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read,profile:read_all,activity:read_all,activity:write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://www.strava.com/oauth/token.

[Official authentication documentation](https://developers.strava.com/docs/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size (default 30; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | `POST /activities` | [docs](https://developers.strava.com/docs/reference/#api-Activities-createActivity) |
| [Get Activity](actions/get-activity.md) | `GET /activities/:id` | [docs](https://developers.strava.com/docs/reference/#api-Activities-getActivityById) |
| [Get Athlete Stats](actions/get-athlete-stats.md) | `GET /athletes/:id/stats` | [docs](https://developers.strava.com/docs/reference/#api-Athletes-getStats) |
| [Get Athlete Zones](actions/get-athlete-zones.md) | `GET /athlete/zones` | [docs](https://developers.strava.com/docs/reference/#api-Athletes-getLoggedInAthleteZones) |
| [Get Authenticated Athlete](actions/get-authenticated-athlete.md) | `GET /athlete` | [docs](https://developers.strava.com/docs/reference/#api-Athletes-getLoggedInAthlete) |
| [Get Route](actions/get-route.md) | `GET /routes/:id` | [docs](https://developers.strava.com/docs/reference/#api-Routes-getRouteById) |
| [Get Segment](actions/get-segment.md) | `GET /segments/:id` | [docs](https://developers.strava.com/docs/reference/#api-Segments-getSegmentById) |
| [Get Upload](actions/get-upload.md) | `GET /uploads/:uploadId` | [docs](https://developers.strava.com/docs/reference/#api-Uploads-getUploadById) |
| [List Activity Comments](actions/list-activity-comments.md) | `GET /activities/:id/comments` | [docs](https://developers.strava.com/docs/reference/#api-Activities-getCommentsByActivityId) |
| [List Activity Kudoers](actions/list-activity-kudoers.md) | `GET /activities/:id/kudos` | [docs](https://developers.strava.com/docs/reference/#api-Activities-getKudoersByActivityId) |
| [List Athlete Activities](actions/list-athlete-activities.md) | `GET /athlete/activities` | [docs](https://developers.strava.com/docs/reference/#api-Activities-getLoggedInAthleteActivities) |
| [List Athlete Clubs](actions/list-athlete-clubs.md) | `GET /athlete/clubs` | [docs](https://developers.strava.com/docs/reference/#api-Clubs-getLoggedInAthleteClubs) |
| [List Athlete Routes](actions/list-athlete-routes.md) | `GET /athletes/:id/routes` | [docs](https://developers.strava.com/docs/reference/#api-Routes-getRoutesByAthleteId) |
| [Update Activity](actions/update-activity.md) | `PUT /activities/:id` | [docs](https://developers.strava.com/docs/reference/#api-Activities-updateActivityById) |
| [Upload Activity](actions/upload-activity.md) | `POST /uploads` | [docs](https://developers.strava.com/docs/reference/#api-Uploads-createUpload) |
