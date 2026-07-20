# Office Ladies Podcast: Native API Reference

A consolidated summary of Office Ladies Podcast's API configuration, with links to official documentation.

- **Official docs:** https://officeladies.com/subscribe
- **API base URL:** `https://feeds.megaphone.fm`

## Authentication

### No authentication

The Office Ladies podcast feed is public and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://officeladies.com/subscribe)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml, application/xml;q=0.9, */*;q=0.8` |

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.
