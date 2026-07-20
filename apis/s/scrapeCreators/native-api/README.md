# Scrape Creators: Native API Reference

A consolidated summary of Scrape Creators's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://docs.scrapecreators.com
- **OpenAPI specification:** https://docs.scrapecreators.com/openapi.json
- **API base URL:** `https://api.scrapecreators.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.scrapecreators.com)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /v1/credit-balance` | [docs](https://docs.scrapecreators.com/v1/credit-balance/) |
| [Get Facebook Profile](actions/get-facebook-profile.md) | `GET /v1/facebook/profile` | [docs](https://docs.scrapecreators.com/v1/facebook/profile/) |
| [Get Google Search Results](actions/get-google-search-results.md) | `GET /v1/google/search` | [docs](https://docs.scrapecreators.com/v1/google/search/) |
| [Get Instagram Basic Profile](actions/get-instagram-basic-profile.md) | `GET /v1/instagram/basic-profile` | [docs](https://docs.scrapecreators.com/v1/instagram/basic-profile/) |
| [Get LinkedIn Company Page](actions/get-linked-in-company-page.md) | `GET /v1/linkedin/company` | [docs](https://docs.scrapecreators.com/v1/linkedin/company/) |
| [Get LinkedIn Profile](actions/get-linked-in-profile.md) | `GET /v1/linkedin/profile` | [docs](https://docs.scrapecreators.com/v1/linkedin/profile/) |
| [Get Linkme Profile](actions/get-linkme-profile.md) | `GET /v1/linkme` | [docs](https://docs.scrapecreators.com/v1/linkme/) |
| [Get Linktree Page](actions/get-linktree-page.md) | `GET /v1/linktree` | [docs](https://docs.scrapecreators.com/v1/linktree/) |
| [Get Snapchat User Profile](actions/get-snapchat-user-profile.md) | `GET /v1/snapchat/profile` | [docs](https://docs.scrapecreators.com/v1/snapchat/profile/) |
| [Get Threads Profile](actions/get-threads-profile.md) | `GET /v1/threads/profile` | [docs](https://docs.scrapecreators.com/v1/threads/profile/) |
| [Get TikTok Profile](actions/get-tik-tok-profile.md) | `GET /v1/tiktok/profile` | [docs](https://docs.scrapecreators.com/v1/tiktok/profile/) |
| [Get TikTok Song Details](actions/get-tik-tok-song-details.md) | `GET /v1/tiktok/song` | [docs](https://docs.scrapecreators.com/v1/tiktok/song/) |
| [Get TikTok Transcript](actions/get-tik-tok-transcript.md) | `GET /v1/tiktok/video/transcript` | [docs](https://docs.scrapecreators.com/v1/tiktok/video/transcript/) |
| [Get TikTok Trending Feed](actions/get-tik-tok-trending-feed.md) | `GET /v1/tiktok/get-trending-feed` | [docs](https://docs.scrapecreators.com/v1/tiktok/get-trending-feed/) |
| [Get TikTok Video Info](actions/get-tik-tok-video-info.md) | `GET /v2/tiktok/video` | [docs](https://docs.scrapecreators.com/v2/tiktok/video/) |
| [Get Twitter Profile](actions/get-twitter-profile.md) | `GET /v1/twitter/profile` | [docs](https://docs.scrapecreators.com/v1/twitter/profile/) |
| [Get YouTube Transcript](actions/get-you-tube-transcript.md) | `GET /v1/youtube/video/transcript` | [docs](https://docs.scrapecreators.com/v1/youtube/video/transcript/) |
| [Get YouTube Trending Shorts](actions/get-you-tube-trending-shorts.md) | `GET /v1/youtube/shorts/trending` | [docs](https://docs.scrapecreators.com/v1/youtube/shorts/trending/) |
| [Get YouTube Video Details](actions/get-you-tube-video-details.md) | `GET /v1/youtube/video` | [docs](https://docs.scrapecreators.com/v1/youtube/video/) |
