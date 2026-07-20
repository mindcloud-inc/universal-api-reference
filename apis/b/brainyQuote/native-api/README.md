# BrainyQuote: Native API Reference

A consolidated summary of BrainyQuote's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.brainyquote.com/feeds/todays_quote
- **API base URL:** `https://www.brainyquote.com`

## Authentication

### No authentication

BrainyQuote RSS feeds are public and do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.brainyquote.com/feeds/todays_quote)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml, application/xml, text/xml;q=0.9, */*;q=0.8` |

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Art Quote of the Day](actions/get-art-quote-of-the-day.md) | `GET /link/quotear.rss` | [docs](https://www.brainyquote.com/feeds/art) |
| [Get Funny Quote of the Day](actions/get-funny-quote-of-the-day.md) | `GET /link/quotefu.rss` | [docs](https://www.brainyquote.com/feeds/funny) |
| [Get Love Quote of the Day](actions/get-love-quote-of-the-day.md) | `GET /link/quotelo.rss` | [docs](https://www.brainyquote.com/feeds/love) |
| [Get Nature Quote of the Day](actions/get-nature-quote-of-the-day.md) | `GET /link/quotena.rss` | [docs](https://www.brainyquote.com/feeds/nature) |
| [Get Today's Quotes](actions/get-todays-quotes.md) | `GET /link/quotebr.rss` | [docs](https://www.brainyquote.com/feeds/todays_quote) |
