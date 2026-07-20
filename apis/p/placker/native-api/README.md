# Placker: Native API Reference

A consolidated summary of Placker's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://placker.com/docs/api/index.html
- **OpenAPI specification:** https://placker.com/docs/api/openapi.yaml
- **API base URL:** `https://api.placker.com`

## Authentication

### API Key

Connect Placker with the raw API key from your Placker profile. Paste only the single-line key value with no quotes or line breaks.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://placker.com/docs/api/common/info.yaml)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–50). Use `offset` in the query string as the record offset.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Card Comment](actions/add-card-comment.md) | `PUT /card/:card/comment` | [docs](https://placker.com/docs/api/paths/card.yaml) |
| [Add Card Label](actions/add-card-label.md) | `PUT /card/:card/label` | [docs](https://placker.com/docs/api/paths/card.yaml) |
| [Add Card Member](actions/add-card-member.md) | `PUT /card/:card/member` | [docs](https://placker.com/docs/api/paths/card.yaml) |
| [Create Card On List](actions/create-card-on-list.md) | `POST /list/:list/card` | [docs](https://placker.com/docs/api/paths/list.yaml) |
| [Create Checklist Item](actions/create-checklist-item.md) | `POST /checklist/:checklist/item` | [docs](https://placker.com/docs/api/paths/checklist.yaml) |
| [Create Checklist On Card](actions/create-checklist-on-card.md) | `POST /card/:card/checklist` | [docs](https://placker.com/docs/api/paths/card.yaml) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhook/:board` | [docs](https://placker.com/docs/api/paths/webhook.yaml) |
| [Delete Checklist](actions/delete-checklist.md) | `DELETE /checklist/:checklist` | [docs](https://placker.com/docs/api/paths/checklist.yaml) |
| [Delete Checklist Item](actions/delete-checklist-item.md) | `DELETE /checklist/:checklist/item/:item` | [docs](https://placker.com/docs/api/paths/checklist.yaml) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhook/:board/:webhook` | [docs](https://placker.com/docs/api/paths/webhook.yaml) |
| [Get Board Details](actions/get-board-details.md) | `GET /board/:board` | [docs](https://placker.com/docs/api/paths/board.yaml) |
| [Get Card Details](actions/get-card-details.md) | `GET /card/:card` | [docs](https://placker.com/docs/api/paths/card.yaml) |
| [Get Checklist Details](actions/get-checklist-details.md) | `GET /checklist/:checklist` | [docs](https://placker.com/docs/api/paths/checklist.yaml) |
| [Get Webhook Example Data](actions/get-webhook-example-data.md) | `GET /webhook/:board/example` | [docs](https://placker.com/docs/api/paths/webhook.yaml) |
| [List Board Attributes](actions/list-board-attributes.md) | `GET /board/:board/attribute` | [docs](https://placker.com/docs/api/paths/board.yaml) |
| [List Board Labels](actions/list-board-labels.md) | `GET /board/:board/label` | [docs](https://placker.com/docs/api/paths/board.yaml) |
| [List Board Members](actions/list-board-members.md) | `GET /board/:board/member` | [docs](https://placker.com/docs/api/paths/board.yaml) |
| [List Boards](actions/list-boards.md) | `GET /board` | [docs](https://placker.com/docs/api/paths/board.yaml) |
| [List Card Checklists](actions/list-card-checklists.md) | `GET /card/:card/checklist` | [docs](https://placker.com/docs/api/paths/card.yaml) |
| [List Card Comments](actions/list-card-comments.md) | `GET /card/:card/comment` | [docs](https://placker.com/docs/api/paths/card.yaml) |
| [List Cards On Board](actions/list-cards-on-board.md) | `GET /board/:board/card` | [docs](https://placker.com/docs/api/paths/board.yaml) |
| [List Cards On List](actions/list-cards-on-list.md) | `GET /list/:list/card` | [docs](https://placker.com/docs/api/paths/list.yaml) |
| [List Lists On Board](actions/list-lists-on-board.md) | `GET /board/:board/list` | [docs](https://placker.com/docs/api/paths/board.yaml) |
| [List User Notifications](actions/list-user-notifications.md) | `GET /me/notifications` | [docs](https://placker.com/docs/api/paths/me.yaml) |
| [Mirror Card To Card](actions/mirror-card-to-card.md) | `POST /card/:card/mirror/card` | [docs](https://placker.com/docs/api/paths/mirror.yaml) |
| [Mirror Card To Checklist Item](actions/mirror-card-to-checklist-item.md) | `POST /card/:card/mirror/item` | [docs](https://placker.com/docs/api/paths/mirror.yaml) |
| [Mirror Checklist Item To Card](actions/mirror-checklist-item-to-card.md) | `POST /checklist/:checklist/item/:item/mirror/card` | [docs](https://placker.com/docs/api/paths/mirror.yaml) |
| [Remove Card Label](actions/remove-card-label.md) | `DELETE /card/:card/label/:label` | [docs](https://placker.com/docs/api/paths/card.yaml) |
| [Remove Card Member](actions/remove-card-member.md) | `DELETE /card/:card/member/:member` | [docs](https://placker.com/docs/api/paths/card.yaml) |
| [Search Cards](actions/search-cards.md) | `GET /card` | [docs](https://placker.com/docs/api/paths/card.yaml) |
| [Update Card](actions/update-card.md) | `PATCH /card/:card` | [docs](https://placker.com/docs/api/paths/card.yaml) |
| [Update Checklist](actions/update-checklist.md) | `PATCH /checklist/:checklist` | [docs](https://placker.com/docs/api/paths/checklist.yaml) |
| [Update Checklist Item](actions/update-checklist-item.md) | `PATCH /checklist/:checklist/item/:item` | [docs](https://placker.com/docs/api/paths/checklist.yaml) |
