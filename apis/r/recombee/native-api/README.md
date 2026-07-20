# Recombee: Native API Reference

A consolidated summary of Recombee's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.recombee.com/api
- **API base URL:** `https://rapi.recombee.com/{databaseId}`

## Authentication

### Recombee API Key

Use your Recombee database ID and private token.

### Credentials

- **API Key:** `apiKey` · required
- **Database ID:** `databaseId` · required · Your Recombee database ID.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.recombee.com/authentication)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Bookmark](actions/add-bookmark.md) | `POST /bookmarks/` | [docs](https://docs.recombee.com/api) |
| [Add Cart Addition](actions/add-cart-addition.md) | `POST /cartadditions/` | [docs](https://docs.recombee.com/api) |
| [Add Detail View](actions/add-detail-view.md) | `POST /detailviews/` | [docs](https://docs.recombee.com/api) |
| [Add Item](actions/add-item.md) | `PUT /items/:itemId` | [docs](https://docs.recombee.com/api) |
| [Add Item Property](actions/add-item-property.md) | `PUT /items/properties/:propertyName` | [docs](https://docs.recombee.com/api) |
| [Add Purchase](actions/add-purchase.md) | `POST /purchases/` | [docs](https://docs.recombee.com/api) |
| [Add Rating](actions/add-rating.md) | `POST /ratings/` | [docs](https://docs.recombee.com/api) |
| [Add Series](actions/add-series.md) | `PUT /series/:seriesId` | [docs](https://docs.recombee.com/api) |
| [Add User](actions/add-user.md) | `PUT /users/:userId` | [docs](https://docs.recombee.com/api) |
| [Add User Property](actions/add-user-property.md) | `PUT /users/properties/:propertyName` | [docs](https://docs.recombee.com/api) |
| [Batch](actions/batch.md) | `POST /batch/` | [docs](https://docs.recombee.com/api) |
| [Get Item Property Info](actions/get-item-property-info.md) | `GET /items/properties/:propertyName` | [docs](https://docs.recombee.com/api) |
| [Get Item Values](actions/get-item-values.md) | `GET /items/:itemId` | [docs](https://docs.recombee.com/api) |
| [Get User Property Info](actions/get-user-property-info.md) | `GET /users/properties/:propertyName` | [docs](https://docs.recombee.com/api) |
| [Get User Values](actions/get-user-values.md) | `GET /users/:userId` | [docs](https://docs.recombee.com/api) |
| [Insert to Series](actions/insert-to-series.md) | `POST /series/:seriesId/items/` | [docs](https://docs.recombee.com/api) |
| [List Item Properties](actions/list-item-properties.md) | `GET /items/properties/list/` | [docs](https://docs.recombee.com/api) |
| [List Items](actions/list-items.md) | `GET /items/list/` | [docs](https://docs.recombee.com/api) |
| [List Series](actions/list-series.md) | `GET /series/list/` | [docs](https://docs.recombee.com/api) |
| [List Series Items](actions/list-series-items.md) | `GET /series/:seriesId/items/` | [docs](https://docs.recombee.com/api) |
| [List User Properties](actions/list-user-properties.md) | `GET /users/properties/list/` | [docs](https://docs.recombee.com/api) |
| [List Users](actions/list-users.md) | `GET /users/list/` | [docs](https://docs.recombee.com/api) |
| [Merge Users](actions/merge-users.md) | `PUT /users/:targetUserId/merge/:sourceUserId` | [docs](https://docs.recombee.com/api) |
| [Recommend Items to Item](actions/recommend-items-to-item.md) | `POST /recomms/items/:itemId/items/` | [docs](https://docs.recombee.com/api) |
| [Recommend Items to User](actions/recommend-items-to-user.md) | `POST /recomms/users/:userId/items/` | [docs](https://docs.recombee.com/api) |
| [Search Items](actions/search-items.md) | `POST /search/users/:userId/items/` | [docs](https://docs.recombee.com/api) |
| [Set Item Values](actions/set-item-values.md) | `POST /items/:itemId` | [docs](https://docs.recombee.com/api) |
| [Set User Values](actions/set-user-values.md) | `POST /users/:userId` | [docs](https://docs.recombee.com/api) |
| [Set View Portion](actions/set-view-portion.md) | `POST /viewportions/` | [docs](https://docs.recombee.com/api) |
| [Update More Items](actions/update-more-items.md) | `POST /more-items/` | [docs](https://docs.recombee.com/api) |
