# The Bible In A Year: Native API Reference

A consolidated summary of The Bible In A Year's API configuration, with links to official documentation.

- **Official docs:** https://ifttt.com/bible/triggers/today_s_episode
- **API base URL:** `https://feeds.fireside.fm`

## Authentication

### No Authentication

The official Fireside RSS feed for The Bible In A Year podcast is publicly readable and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://feeds.fireside.fm/bibleinayear/rss)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml, application/xml, text/xml` |

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
