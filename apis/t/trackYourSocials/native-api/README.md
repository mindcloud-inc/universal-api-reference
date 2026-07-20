# TrackYourSocials: Native API Reference

A consolidated summary of TrackYourSocials's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://trackyoursocials.com/docs
- **API base URL:** `https://trackyoursocials.com`

## Authentication

### API Key

Authenticate TrackYourSocials requests with a dashboard-generated API key sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://trackyoursocials.com/docs)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Post Analytics](actions/get-post-analytics.md) | `GET /api/v1/analytics` | [docs](https://trackyoursocials.com/docs) |
| [List Last N Posts](actions/list-last-n-posts.md) | `GET /api/v1/last-n-posts` | [docs](https://trackyoursocials.com/docs) |
| [List Previous Day Posts](actions/list-previous-day-posts.md) | `GET /api/v1/previous-day-posts` | [docs](https://trackyoursocials.com/docs) |
