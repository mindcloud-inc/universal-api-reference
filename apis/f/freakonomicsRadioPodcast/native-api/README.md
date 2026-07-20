# Freakonomics Radio Podcast: Native API Reference

A consolidated summary of Freakonomics Radio Podcast's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://feeds.simplecast.com/Y8lFbOT4
- **API base URL:** `https://feeds.simplecast.com`

## Authentication

### No Authentication

This app reads the public Freakonomics Radio RSS feed. No provider-managed credentials are required.

This API does not require request authentication.

[Official authentication documentation](https://feeds.simplecast.com/Y8lFbOT4)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml, application/xml, text/xml;q=0.9, application/atom+xml;q=0.8, */*;q=0.1` |

Responses from this API use XML.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Episodes](actions/list-episodes.md) | `GET /Y8lFbOT4` | [docs](https://feeds.simplecast.com/Y8lFbOT4) |
