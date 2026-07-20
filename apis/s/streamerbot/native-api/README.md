# Streamer.bot: Native API Reference

A consolidated summary of Streamer.bot's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.streamer.bot/
- **API base URL:** `https://allow-freely-princess-carefully.trycloudflare.com`

## Authentication

### Local HTTP Server

Connect to a local Streamer.bot HTTP server without provider-managed credentials.

This API does not require request authentication.

[Official authentication documentation](https://docs.streamer.bot/api/http/guide/configuration)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Clear Credits](actions/clear-credits.md) | `GET /ClearCredits` | [docs](https://docs.streamer.bot/api/http/requests/clear-credits) |
| [Clear First Words Cache](actions/clear-first-words-cache.md) | `GET /ClearFirstWordsCache` | [docs](https://docs.streamer.bot/api/http/requests/clear-first-words-cache) |
| [Do Action](actions/do-action.md) | `POST /DoAction` | [docs](https://docs.streamer.bot/api/http/requests/do-action) |
| [Get Actions](actions/get-actions.md) | `GET /GetActions` | [docs](https://docs.streamer.bot/api/http/requests/get-actions) |
| [Get Credits](actions/get-credits.md) | `GET /GetCredits` | [docs](https://docs.streamer.bot/api/http/requests/get-credits) |
| [Test Credits](actions/test-credits.md) | `GET /TestCredits` | [docs](https://docs.streamer.bot/api/http/requests/test-credits) |
