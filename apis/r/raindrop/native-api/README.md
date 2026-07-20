# Raindrop: Native API Reference

A consolidated summary of Raindrop's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.raindrop.io/
- **API base URL:** `https://api.raindrop.io/rest/v1`

## Authentication

### OAuth2

Connect Raindrop using the provider OAuth app flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://raindrop.io/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://raindrop.io/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `.`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://raindrop.io/oauth/access_token.

[Official authentication documentation](https://developer.raindrop.io/v1/authentication/token)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Highlight](actions/add-highlight.md) | `PUT /raindrop/:id` | [docs](https://developer.raindrop.io/v1/highlights) |
| [Create Collection](actions/create-collection.md) | `POST /collection` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Create Raindrop](actions/create-raindrop.md) | `POST /raindrop` | [docs](https://developer.raindrop.io/v1/raindrops/single) |
| [Delete Collection](actions/delete-collection.md) | `DELETE /collection/:id` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Empty Trash](actions/empty-trash.md) | `DELETE /collection/-99` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Generate Backup](actions/generate-backup.md) | `GET /backup` | [docs](https://developer.raindrop.io/v1/backups) |
| [Get All Backups](actions/get-all-backups.md) | `GET /backups` | [docs](https://developer.raindrop.io/v1/backups) |
| [Get All Highlights](actions/get-all-highlights.md) | `GET /highlights` | [docs](https://developer.raindrop.io/v1/highlights) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /user` | [docs](https://developer.raindrop.io/v1/user/authenticated) |
| [Get Child Collections](actions/get-child-collections.md) | `GET /collections/childrens` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Get Collection](actions/get-collection.md) | `GET /collection/:id` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Get Collection Highlights](actions/get-collection-highlights.md) | `GET /highlights/:collectionId` | [docs](https://developer.raindrop.io/v1/highlights) |
| [Get Featured Collection Covers](actions/get-featured-collection-covers.md) | `GET /collections/covers` | [docs](https://developer.raindrop.io/v1/collections/covers-icons) |
| [Get Filters](actions/get-filters.md) | `GET /filters/:collectionId` | [docs](https://developer.raindrop.io/v1/filters) |
| [Get Public User](actions/get-public-user.md) | `GET /user/:name` | [docs](https://developer.raindrop.io/v1/user/authenticated) |
| [Get Raindrop](actions/get-raindrop.md) | `GET /raindrop/:id` | [docs](https://developer.raindrop.io/v1/raindrops/single) |
| [Get Raindrops](actions/get-raindrops.md) | `GET /raindrops/:collectionId` | [docs](https://developer.raindrop.io/v1/raindrops/multiple) |
| [Get Root Collections](actions/get-root-collections.md) | `GET /collections` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Get System Collection Counts](actions/get-system-collection-counts.md) | `GET /user/stats` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Get Tags](actions/get-tags.md) | `GET /tags/:collectionId` | [docs](https://developer.raindrop.io/v1/tags) |
| [Merge Collections](actions/merge-collections.md) | `PUT /collections/merge` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Parse URL](actions/parse-url.md) | `GET /import/url/parse` | [docs](https://developer.raindrop.io/v1/import) |
| [Remove Empty Collections](actions/remove-empty-collections.md) | `PUT /collections/clean` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Remove Highlight](actions/remove-highlight.md) | `PUT /raindrop/:id` | [docs](https://developer.raindrop.io/v1/highlights) |
| [Remove Multiple Collections](actions/remove-multiple-collections.md) | `DELETE /collections` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Reorder All Collections](actions/reorder-all-collections.md) | `PUT /collections` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Search Collection Covers](actions/search-collection-covers.md) | `GET /collections/covers/:text` | [docs](https://developer.raindrop.io/v1/collections/covers-icons) |
| [Set Collections Expanded State](actions/set-collections-expanded-state.md) | `PUT /collections` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Update Collection](actions/update-collection.md) | `PUT /collection/:id` | [docs](https://developer.raindrop.io/v1/collections/methods) |
| [Update Highlight](actions/update-highlight.md) | `PUT /raindrop/:id` | [docs](https://developer.raindrop.io/v1/highlights) |
