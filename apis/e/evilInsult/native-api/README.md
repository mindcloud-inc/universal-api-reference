# Evil Insult: Native API Reference

A consolidated summary of Evil Insult's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://evilinsult.com/api
- **API base URL:** `https://evilinsult.com`

## Authentication

### No authentication

The Evil Insult Generator documented endpoint is public and does not use credentials.

This API does not require request authentication.

[Official authentication documentation](https://evilinsult.com/api)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 250 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Insult (JSON)](actions/generate-insult-json.md) | `GET /generate_insult.php` | [docs](https://evilinsult.com/api) |
| [Generate Insult (Text)](actions/generate-insult-text.md) | `GET /generate_insult.php` | [docs](https://evilinsult.com/api) |
| [Generate Insult (XML)](actions/generate-insult-xml.md) | `GET /generate_insult.php` | [docs](https://evilinsult.com/api) |
