# RSS Feed: Native API Reference

A consolidated summary of RSS Feed's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.rssboard.org/rss-specification
- **API base URL:** `{feedUrl}`

## Authentication

### Feed URL

Provide the RSS feed URL to read. No provider-managed credential is required.

### Credentials

- **Feed URL:** `feedUrl` · required · Full RSS feed URL, for example https://example.com/feed.xml

[Official authentication documentation](https://www.rssboard.org/rss-specification)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml, application/xml, text/xml;q=0.9, application/atom+xml;q=0.8, */*;q=0.1` |

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Feed Items](actions/list-feed-items.md) | `GET {{credentials.feedUrl}}` | [docs](https://www.rssboard.org/rss-specification) |
