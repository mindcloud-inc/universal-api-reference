# EmojiHub: Native API Reference

A consolidated summary of EmojiHub's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://github.com/cheatsnake/emojihub
- **API base URL:** `https://emojihub.yurace.pro/api`

## Authentication

### No Authentication

This API does not require request authentication.

[Official authentication documentation](https://github.com/cheatsnake/emojihub)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Random Emoji](actions/get-random-emoji.md) | `GET /random` | [docs](https://github.com/cheatsnake/emojihub) |
| [Get Random Emoji By Category](actions/get-random-emoji-by-category.md) | `GET /random/category/:category` | [docs](https://github.com/cheatsnake/emojihub) |
| [Get Random Emoji By Group](actions/get-random-emoji-by-group.md) | `GET /random/group/:group` | [docs](https://github.com/cheatsnake/emojihub) |
| [Get Similar Emojis](actions/get-similar-emojis.md) | `GET /similar/:name` | [docs](https://github.com/cheatsnake/emojihub) |
| [List Emoji Categories](actions/list-emoji-categories.md) | `GET /categories` | [docs](https://github.com/cheatsnake/emojihub) |
| [List Emoji Groups](actions/list-emoji-groups.md) | `GET /groups` | [docs](https://github.com/cheatsnake/emojihub) |
| [List Emojis](actions/list-emojis.md) | `GET /all` | [docs](https://github.com/cheatsnake/emojihub) |
| [List Emojis By Category](actions/list-emojis-by-category.md) | `GET /all/category/:category` | [docs](https://github.com/cheatsnake/emojihub) |
| [List Emojis By Group](actions/list-emojis-by-group.md) | `GET /all/group/:group` | [docs](https://github.com/cheatsnake/emojihub) |
| [Search Emojis](actions/search-emojis.md) | `GET /search` | [docs](https://github.com/cheatsnake/emojihub) |
