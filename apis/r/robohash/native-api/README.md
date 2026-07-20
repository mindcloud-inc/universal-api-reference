# Robohash: Native API Reference

A consolidated summary of Robohash's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://github.com/e1ven/Robohash
- **API base URL:** `https://robohash.org`

## Authentication

### No authentication

Robohash is a public URL-based service and does not require API keys, tokens, OAuth, or account credentials.

This API does not require request authentication.

[Official authentication documentation](https://github.com/e1ven/Robohash)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | `GET /:text.:format` | [docs](https://github.com/e1ven/Robohash) |
