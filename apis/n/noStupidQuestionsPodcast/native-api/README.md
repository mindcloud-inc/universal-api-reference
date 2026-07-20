# No Stupid Questions Podcast: Native API Reference

A consolidated summary of No Stupid Questions Podcast's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://feeds.simplecast.com/dfh_verV
- **API base URL:** `https://feeds.simplecast.com/dfh_verV`

## Authentication

### No Authentication

The public No Stupid Questions RSS feed does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://feeds.simplecast.com/dfh_verV)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml` |

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Episodes](actions/list-episodes.md) | `GET` | [docs](https://feeds.simplecast.com/dfh_verV) |
