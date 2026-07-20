# Fathom: Native API Reference

A consolidated summary of Fathom's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://developers.fathom.ai/api-overview
- **API base URL:** `https://api.fathom.ai/external/v1`

## Authentication

### OAuth 2.0

Fathom OAuth2 development credentials.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://fathom.video/external/v1/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://fathom.video/external/v1/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `public_api`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://fathom.video/external/v1/oauth2/token.

[Official authentication documentation](https://developers.fathom.ai/sdks/oauth)

## API conventions

Responses from this API use JSON. Response data is read from `items`. The next-page cursor is read from `next_cursor`.

## Pagination

Use `cursor` in the query string as the pagination cursor; numbering starts at 0.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developers.fathom.ai/api-reference/webhooks/create-a-webhook) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://developers.fathom.ai/api-reference/webhooks/delete-a-webhook) |
| [Get Recording Summary](actions/get-recording-summary.md) | `GET /recordings/:recording_id/summary` | [docs](https://developers.fathom.ai/api-reference/recordings/get-summary) |
| [Get Transcript](actions/get-transcript.md) | `GET /recordings/:recording_id/transcript` | [docs](https://developers.fathom.ai/api-reference/recordings/get-transcript) |
| [List Meetings](actions/list-meetings.md) | `GET /meetings` | [docs](https://developers.fathom.ai/api-reference/meetings/list-meetings) |
| [List Team Members](actions/list-team-members.md) | `GET /team_members` | [docs](https://developers.fathom.ai/api-reference/team-members/list-team-members) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://developers.fathom.ai/api-reference/teams/list-teams) |
