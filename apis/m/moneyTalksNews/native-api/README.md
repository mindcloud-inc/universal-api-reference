# Money Talks News: Native API Reference

A consolidated summary of Money Talks News's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://www.rssboard.org/rss-specification
- **API base URL:** `https://www.moneytalksnews.com`

## Authentication

### Feed URL

Provide the full Money Talks News RSS feed URL used for runtime reads.

### Credentials

- **Feed URL:** `feedUrl` · required · Full RSS feed URL for Money Talks News. Use https://www.moneytalksnews.com/feed/.

[Official authentication documentation](https://www.rssboard.org/rss-specification)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml, application/xml, text/xml;q=0.9, application/atom+xml;q=0.8, */*;q=0.1` |

Responses from this API use XML.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Author Feed Items](actions/list-author-feed-items.md) | `GET /author/:authorSlug/feed/` | [docs](https://www.rssboard.org/rss-specification) |
| [List Category Feed Items](actions/list-category-feed-items.md) | `GET /category/:categorySlug/feed/` | [docs](https://www.rssboard.org/rss-specification) |
| [List Global Comments Feed Items](actions/list-global-comments-feed-items.md) | `GET /comments/feed/` | [docs](https://www.rssboard.org/rss-specification) |
| [List Post Comments Feed Items](actions/list-post-comments-feed-items.md) | `GET /:postSlug/feed/` | [docs](https://www.rssboard.org/rss-specification) |
| [List Search Feed Items](actions/list-search-feed-items.md) | `GET /search/:searchTerm/feed/rss2/` | [docs](https://www.rssboard.org/rss-specification) |
| [List Site Feed Items](actions/list-site-feed-items.md) | `GET /feed/` | [docs](https://www.rssboard.org/rss-specification) |
| [List Tag Feed Items](actions/list-tag-feed-items.md) | `GET /tag/:tagSlug/feed/` | [docs](https://www.rssboard.org/rss-specification) |
