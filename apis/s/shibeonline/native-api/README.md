# Shibe.online: Native API Reference

A consolidated summary of Shibe.online's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://shibe.online/
- **API base URL:** `https://shibe.online`

## Authentication

### No authentication

Shibe.online image endpoints are public and require no credentials.

This API does not require request authentication.

[Official authentication documentation](https://shibe.online/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 250 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Random Bird Images](actions/get-random-bird-images.md) | `GET /api/birds` | [docs](https://shibe.online/) |
| [Get Random Cat Images](actions/get-random-cat-images.md) | `GET /api/cats` | [docs](https://shibe.online/) |
| [Get Random Shibe Images](actions/get-random-shibe-images.md) | `GET /api/shibes` | [docs](https://shibe.online/) |
