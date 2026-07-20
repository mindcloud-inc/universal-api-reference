# Dungeon Fighter Online: Native API Reference

A consolidated summary of Dungeon Fighter Online's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developers.neople.co.kr/contents/apiDocs
- **API base URL:** `https://api.neople.co.kr`

## Authentication

### API Key

Use a Neople Developers API key. The runtime sends it as the `apikey` query parameter for Dungeon & Fighter Open API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.neople.co.kr/contents/guide/pages/all)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Auction Item](actions/get-auction-item.md) | `GET /df/auction/:auctionNo` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Get Avatar Market Sale](actions/get-avatar-market-sale.md) | `GET /df/avatar-market/sale/:goodsNo` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Get Avatar Market Sold Item](actions/get-avatar-market-sold-item.md) | `GET /df/avatar-market/sold/:goodsNo` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Get Item](actions/get-item.md) | `GET /df/items/:itemId` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Get Multiple Items](actions/get-multiple-items.md) | `GET /df/multi/items` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Get Multiple Set Items](actions/get-multiple-set-items.md) | `GET /df/multi/setitems` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Get Multiple Skills](actions/get-multiple-skills.md) | `GET /df/multi/skills/:jobId` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Get Set Item](actions/get-set-item.md) | `GET /df/setitems/:setItemId` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Get Skill](actions/get-skill.md) | `GET /df/skills/:jobId/:skillId` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [List Avatar Market Hashtags](actions/list-avatar-market-hashtags.md) | `GET /df/avatar-market/hashtag` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [List Item Hashtags](actions/list-item-hashtags.md) | `GET /df/item-hashtag` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [List Jobs](actions/list-jobs.md) | `GET /df/jobs` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [List Servers](actions/list-servers.md) | `GET /df/servers` | [docs](https://developers.neople.co.kr/contents/apiDocs) |
| [List Skills](actions/list-skills.md) | `GET /df/skills/:jobId` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Search Auction Items](actions/search-auction-items.md) | `GET /df/auction` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Search Avatar Market Sales](actions/search-avatar-market-sales.md) | `GET /df/avatar-market/sale` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Search Avatar Market Sold Items](actions/search-avatar-market-sold-items.md) | `GET /df/avatar-market/sold` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Search Items](actions/search-items.md) | `GET /df/items` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Search Set Items](actions/search-set-items.md) | `GET /df/setitems` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
| [Search Sold Auction Items](actions/search-sold-auction-items.md) | `GET /df/auction-sold` | [docs](https://developers.neople.co.kr/contents/apiDocs/df) |
