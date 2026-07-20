# Curator: Native API Reference

A consolidated summary of Curator's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://curator.io/docs/api
- **API base URL:** `https://api.curator.io`

## Authentication

### API Key

Connect to Curator with your Curator API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://curator.io/docs/api)

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Ad](actions/create-ad.md) | `POST /v1.2/ads` | [docs](https://curator.io/docs/api/ads) |
| [Create Feed](actions/create-feed.md) | `POST /v1/feeds` | [docs](https://curator.io/docs/api/feeds) |
| [Create Source](actions/create-source.md) | `POST /v1/sources` | [docs](https://curator.io/docs/api/sources) |
| [Delete Ad](actions/delete-ad.md) | `DELETE /v1.2/ads/:AD_ID` | [docs](https://curator.io/docs/api/ads) |
| [Delete Feed](actions/delete-feed.md) | `DELETE /v1/feeds/:FEED_ID` | [docs](https://curator.io/docs/api/feeds) |
| [Delete Source](actions/delete-source.md) | `DELETE /v1/sources/:SOURCE_ID` | [docs](https://curator.io/docs/api/sources) |
| [List Ads](actions/list-ads.md) | `GET /v1.2/ads` | [docs](https://curator.io/docs/api/ads) |
| [List Feeds](actions/list-feeds.md) | `GET /v1/feeds` | [docs](https://curator.io/docs/api/feeds) |
| [List Posts](actions/list-posts.md) | `GET /v1/feeds/:FEED_ID/posts` | [docs](https://curator.io/docs/api/posts) |
| [List Sources](actions/list-sources.md) | `GET /v1/sources` | [docs](https://curator.io/docs/api/sources) |
| [Update Ad](actions/update-ad.md) | `POST /v1.2/ads/:AD_ID` | [docs](https://curator.io/docs/api/ads) |
| [Update Feed](actions/update-feed.md) | `POST /v1/feeds/:FEED_ID` | [docs](https://curator.io/docs/api/feeds) |
| [Update Source](actions/update-source.md) | `POST /v1/sources/:SOURCE_ID` | [docs](https://curator.io/docs/api/sources) |
