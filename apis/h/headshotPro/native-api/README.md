# HeadshotPro: Native API Reference

A consolidated summary of HeadshotPro's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.headshotpro.com/api
- **API base URL:** `https://server.headshotpro.com/api/v2`

## Authentication

### API Key

Authenticate with a HeadshotPro organization API key. HeadshotPro requires Authorization: Bearer <API_KEY> on every request.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.headshotpro.com/api/authentication)

## API conventions

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–200). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Members To Team](actions/add-members-to-team.md) | `POST /organization/teams/:teamId/members` | [docs](https://www.headshotpro.com/api/team-members) |
| [Create Invite](actions/create-invite.md) | `POST /organization/invites` | [docs](https://www.headshotpro.com/api/invites) |
| [Create Model](actions/create-model.md) | `POST /organization/models` | [docs](https://www.headshotpro.com/api/models) |
| [Create Team](actions/create-team.md) | `POST /organization/teams` | [docs](https://www.headshotpro.com/api/teams) |
| [Delete Model](actions/delete-model.md) | `DELETE /organization/models/:modelId` | [docs](https://www.headshotpro.com/api/models) |
| [Delete Team](actions/delete-team.md) | `DELETE /organization/teams/:teamId` | [docs](https://www.headshotpro.com/api/teams) |
| [Download Model Photos](actions/download-model-photos.md) | `POST /organization/models/:modelId/photos/download` | [docs](https://www.headshotpro.com/api/photos) |
| [Get Credits](actions/get-credits.md) | `GET /organization/credits` | [docs](https://www.headshotpro.com/api/organization) |
| [Get Favorite Model Photo](actions/get-favorite-model-photo.md) | `GET /organization/models/:modelId/photos/favorite` | [docs](https://www.headshotpro.com/api/photos) |
| [Get Invite By Email](actions/get-invite-by-email.md) | `GET /organization/invites/:email` | [docs](https://www.headshotpro.com/api/invites) |
| [Get Model](actions/get-model.md) | `GET /organization/models/:modelId` | [docs](https://www.headshotpro.com/api/models) |
| [Get Model Photo](actions/get-model-photo.md) | `GET /organization/models/:modelId/photos/:photoId` | [docs](https://www.headshotpro.com/api/photos) |
| [Get Organization](actions/get-organization.md) | `GET /organization` | [docs](https://www.headshotpro.com/api/organization) |
| [List Accepted Team Members](actions/list-accepted-team-members.md) | `GET /organization/team/accepted` | [docs](https://www.headshotpro.com/api/team-members) |
| [List Favorite Photos](actions/list-favorite-photos.md) | `GET /organization/photos/favorites` | [docs](https://www.headshotpro.com/api/photos) |
| [List Finished Team Members](actions/list-finished-team-members.md) | `GET /organization/team/finished` | [docs](https://www.headshotpro.com/api/team-members) |
| [List Invites](actions/list-invites.md) | `GET /organization/invites` | [docs](https://www.headshotpro.com/api/invites) |
| [List Model Photos](actions/list-model-photos.md) | `GET /organization/models/:modelId/photos` | [docs](https://www.headshotpro.com/api/photos) |
| [List Models](actions/list-models.md) | `GET /organization/models` | [docs](https://www.headshotpro.com/api/models) |
| [List Pending Team Members](actions/list-pending-team-members.md) | `GET /organization/team/pending` | [docs](https://www.headshotpro.com/api/team-members) |
| [List Team Members](actions/list-team-members.md) | `GET /organization/team` | [docs](https://www.headshotpro.com/api/team-members) |
| [List Teams](actions/list-teams.md) | `GET /organization/teams` | [docs](https://www.headshotpro.com/api/teams) |
| [Revoke Invite](actions/revoke-invite.md) | `POST /organization/invites/revoke` | [docs](https://www.headshotpro.com/api/invites) |
| [Update Team](actions/update-team.md) | `PUT /organization/teams/:teamId` | [docs](https://www.headshotpro.com/api/teams) |
