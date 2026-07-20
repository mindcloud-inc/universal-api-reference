# Miro: Native API Reference

A consolidated summary of Miro's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://developers.miro.com/reference
- **API base URL:** `https://api.miro.com/v2`

## Authentication

### OAuth 2.0

Connect a Miro app using OAuth 2.0 client credentials.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://miro.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.miro.com/v1/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `boards:read boards:write`.

Refresh expired access tokens with a POST request to https://api.miro.com/v1/oauth/token.

[Official authentication documentation](https://developers.miro.com/docs/getting-started-with-oauth)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Board](actions/create-board.md) | `POST /boards` | [docs](https://developers.miro.com/reference/create-board) |
| [Create Card](actions/create-card.md) | `POST /boards/:board_id/cards` | [docs](https://developers.miro.com/reference/create-card-item) |
| [Create Sticky Note](actions/create-sticky-note.md) | `POST /boards/:board_id/sticky_notes` | [docs](https://developers.miro.com/reference/create-sticky-note-item) |
| [Create Text](actions/create-text.md) | `POST /boards/:board_id/texts` | [docs](https://developers.miro.com/reference/create-text-item) |
| [Delete Board](actions/delete-board.md) | `DELETE /boards/:board_id` | [docs](https://developers.miro.com/reference/delete-board) |
| [Delete Card](actions/delete-card.md) | `DELETE /boards/:board_id/cards/:item_id` | [docs](https://developers.miro.com/reference/delete-card-item) |
| [Delete Item](actions/delete-item.md) | `DELETE /boards/:board_id/items/:item_id` | [docs](https://developers.miro.com/reference/delete-item) |
| [Delete Sticky Note](actions/delete-sticky-note.md) | `DELETE /boards/:board_id/sticky_notes/:item_id` | [docs](https://developers.miro.com/reference/delete-sticky-note-item) |
| [Delete Text](actions/delete-text.md) | `DELETE /boards/:board_id/texts/:item_id` | [docs](https://developers.miro.com/reference/delete-text-item) |
| [Get Access Token Context](actions/get-access-token-context.md) | `GET https://api.miro.com/v1/oauth-token` | [docs](https://developers.miro.com/reference/get-access-token-context) |
| [Get Board](actions/get-board.md) | `GET /boards/:board_id` | [docs](https://developers.miro.com/reference/get-specific-board) |
| [Get Card](actions/get-card.md) | `GET /boards/:board_id/cards/:item_id` | [docs](https://developers.miro.com/reference/get-card-item) |
| [Get Item](actions/get-item.md) | `GET /boards/:board_id/items/:item_id` | [docs](https://developers.miro.com/reference/get-specific-item) |
| [Get Sticky Note](actions/get-sticky-note.md) | `GET /boards/:board_id/sticky_notes/:item_id` | [docs](https://developers.miro.com/reference/get-sticky-note-item) |
| [Get Text](actions/get-text.md) | `GET /boards/:board_id/texts/:item_id` | [docs](https://developers.miro.com/reference/get-text-item) |
| [List Board Members](actions/list-board-members.md) | `GET /boards/:board_id/members` | [docs](https://developers.miro.com/reference/get-board-members) |
| [List Boards](actions/list-boards.md) | `GET /boards` | [docs](https://developers.miro.com/reference/get-boards) |
| [List Items](actions/list-items.md) | `GET /boards/:board_id/items` | [docs](https://developers.miro.com/reference/get-items) |
| [Remove Board Member](actions/remove-board-member.md) | `DELETE /boards/:board_id/members/:board_member_id` | [docs](https://developers.miro.com/reference/remove-board-member) |
| [Share Board](actions/share-board.md) | `POST /boards/:board_id/members` | [docs](https://developers.miro.com/reference/share-board) |
| [Update Board](actions/update-board.md) | `PATCH /boards/:board_id` | [docs](https://developers.miro.com/reference/update-board) |
| [Update Card](actions/update-card.md) | `PATCH /boards/:board_id/cards/:item_id` | [docs](https://developers.miro.com/reference/update-card-item) |
| [Update Item Position](actions/update-item-position.md) | `PATCH /boards/:board_id/items/:item_id` | [docs](https://developers.miro.com/reference/update-item-position-or-parent) |
| [Update Sticky Note](actions/update-sticky-note.md) | `PATCH /boards/:board_id/sticky_notes/:item_id` | [docs](https://developers.miro.com/reference/update-sticky-note-item) |
| [Update Text](actions/update-text.md) | `PATCH /boards/:board_id/texts/:item_id` | [docs](https://developers.miro.com/reference/update-text-item) |
