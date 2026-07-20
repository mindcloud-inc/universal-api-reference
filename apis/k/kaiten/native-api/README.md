# Kaiten: Native API Reference

A consolidated summary of Kaiten's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.kaiten.ru/
- **API base URL:** `https://{companyDomain}.kaiten.ru/api/latest`

## Authentication

### API Key

Use a Kaiten API key together with your Kaiten company domain.

### Credentials

- **API Key:** `apiKey` · required
- **Company Domain:** `companyDomain` · required · Your Kaiten workspace subdomain without .kaiten.ru, for example acme

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.kaiten.ru/)

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | `POST /cards/:cardId/comments` | [docs](https://developers.kaiten.ru/cards/{card_id}/comments) |
| [Add Member to Card](actions/add-member-to-card.md) | `POST /cards/:cardId/members` | [docs](https://developers.kaiten.ru/cards/{card_id}/members) |
| [Add Tag](actions/add-tag.md) | `POST /tags` | [docs](https://developers.kaiten.ru/tags) |
| [Add Tag to Card](actions/add-tag-to-card.md) | `POST /cards/:cardId/tags` | [docs](https://developers.kaiten.ru/cards/{card_id}/tags) |
| [Create Card](actions/create-card.md) | `POST /cards` | [docs](https://developers.kaiten.ru/cards/create-new-card) |
| [Delete Card](actions/delete-card.md) | `DELETE /cards/:cardId` | [docs](https://developers.kaiten.ru/cards/{card_id}) |
| [Remove Comment](actions/remove-comment.md) | `DELETE /cards/:cardId/comments/:commentId` | [docs](https://developers.kaiten.ru/cards/{card_id}/comments/{comment_id}) |
| [Remove Member from Card](actions/remove-member-from-card.md) | `DELETE /cards/:cardId/members/:id` | [docs](https://developers.kaiten.ru/cards/{card_id}/members/{id}) |
| [Remove Tag from Card](actions/remove-tag-from-card.md) | `DELETE /cards/:cardId/tags/:tagId` | [docs](https://developers.kaiten.ru/cards/{card_id}/tags/{tag_id}) |
| [Retrieve Board](actions/retrieve-board.md) | `GET /spaces/:spaceId/boards/:boardId` | [docs](https://developers.kaiten.ru/space-boards/get-board) |
| [Retrieve Card](actions/retrieve-card.md) | `GET /cards/:cardId` | [docs](https://developers.kaiten.ru/cards/get-card) |
| [Retrieve Card Comments](actions/retrieve-card-comments.md) | `GET /cards/:cardId/comments` | [docs](https://developers.kaiten.ru/cards/{card_id}/comments) |
| [Retrieve Current User](actions/retrieve-current-user.md) | `GET /users/current` | [docs](https://developers.kaiten.ru/users/retrieve-current-user) |
| [Retrieve List of Boards](actions/retrieve-list-of-boards.md) | `GET /spaces/:spaceId/boards` | [docs](https://developers.kaiten.ru/space-boards/get-list-of-boards) |
| [Retrieve List of Card Members](actions/retrieve-list-of-card-members.md) | `GET /cards/:cardId/members` | [docs](https://developers.kaiten.ru/cards/{card_id}/members) |
| [Retrieve List of Card Tags](actions/retrieve-list-of-card-tags.md) | `GET /cards/:cardId/tags` | [docs](https://developers.kaiten.ru/cards/{card_id}/tags) |
| [Retrieve List of Cards](actions/retrieve-list-of-cards.md) | `GET /cards` | [docs](https://developers.kaiten.ru/cards/get-list-of-cards) |
| [Retrieve List of Spaces](actions/retrieve-list-of-spaces.md) | `GET /spaces` | [docs](https://developers.kaiten.ru/spaces/get-list-of-spaces) |
| [Retrieve List of Tags](actions/retrieve-list-of-tags.md) | `GET /tags` | [docs](https://developers.kaiten.ru/tags/retrieve-list-of-tags) |
| [Retrieve List of Users](actions/retrieve-list-of-users.md) | `GET /users` | [docs](https://developers.kaiten.ru/users/retrieve-list-of-users) |
| [Retrieve Space](actions/retrieve-space.md) | `GET /spaces/:spaceId` | [docs](https://developers.kaiten.ru/spaces/get-space) |
| [Update Card](actions/update-card.md) | `PATCH /cards/:cardId` | [docs](https://developers.kaiten.ru/cards/{card_id}) |
| [Update Comment](actions/update-comment.md) | `PATCH /cards/:cardId/comments/:commentId` | [docs](https://developers.kaiten.ru/cards/{card_id}/comments/{comment_id}) |
| [Update Member Role](actions/update-member-role.md) | `PATCH /cards/:cardId/members/:id` | [docs](https://developers.kaiten.ru/cards/{card_id}/members/{id}) |
