# FullSession: Native API Reference

A consolidated summary of FullSession's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://help.fullsession.io/en/collections/14227501-apis-documentation
- **API base URL:** `https://app.fullsession.io/v1/external`

## Authentication

### API Key

Connect with a FullSession API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.fullsession.io/en/articles/11860251-retrieve-website-sessions-api)

## API conventions

Response data is read from `data.sessions`. The next-page cursor is read from `data.startAfter`.

## Pagination

Use `startAfter` in the query string as the pagination cursor.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Website Sessions](actions/list-website-sessions.md) | `GET /sessions/:customerId/:siteId` | [docs](https://help.fullsession.io/en/articles/11860251-retrieve-website-sessions-api) |
