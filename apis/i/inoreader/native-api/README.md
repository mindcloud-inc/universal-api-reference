# Inoreader: Native API Reference

A consolidated summary of Inoreader's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://www.inoreader.com/developers/
- **API base URL:** `https://www.inoreader.com/reader/api/0`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.inoreader.com/oauth2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://www.inoreader.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://www.inoreader.com/oauth2/token.

[Official authentication documentation](https://www.inoreader.com/sk/developers/oauth)

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Feed](actions/add-feed.md) | `POST /subscription/quickadd` | [docs](https://www.inoreader.com/developers/add-subscription) |
| [Delete Tag](actions/delete-tag.md) | `POST /disable-tag` | [docs](https://www.inoreader.com/developers/delete-tag) |
| [Get User Information](actions/get-user-information.md) | `GET /user-info` | [docs](https://www.inoreader.com/developers/user-info) |
| [List Feeds](actions/list-feeds.md) | `GET /subscription/list` | [docs](https://www.inoreader.com/developers/subscription-list) |
| [List Folders and Tags](actions/list-folders-and-tags.md) | `GET /tag/list` | [docs](https://www.inoreader.com/developers/tag-list) |
| [List Stream Contents](actions/list-stream-contents.md) | `GET /stream/contents/:streamId` | [docs](https://www.inoreader.com/developers/stream-contents) |
| [List Stream Item IDs](actions/list-stream-item-ids.md) | `GET /stream/items/ids` | [docs](https://www.inoreader.com/developers/item-ids) |
| [List Stream Preferences](actions/list-stream-preferences.md) | `GET /preference/stream/list` | [docs](https://www.inoreader.com/developers/preference-list) |
| [List Unread Counters](actions/list-unread-counters.md) | `GET /unread-count` | [docs](https://www.inoreader.com/developers/unread-counts) |
| [Mark Stream As Read](actions/mark-stream-as-read.md) | `POST /mark-all-as-read` | [docs](https://www.inoreader.com/developers/mark-all-as-read) |
| [Rename Tag](actions/rename-tag.md) | `POST /rename-tag` | [docs](https://www.inoreader.com/developers/rename-tag) |
| [Update Article Tags](actions/update-article-tags.md) | `POST /edit-tag` | [docs](https://www.inoreader.com/developers/edit-tag) |
| [Update Feed](actions/update-feed.md) | `POST /subscription/edit` | [docs](https://www.inoreader.com/developers/edit-subscription) |
