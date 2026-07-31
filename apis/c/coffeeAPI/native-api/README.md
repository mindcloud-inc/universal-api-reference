# Coffee API: Native API Reference

A consolidated summary of Coffee API's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://coffee.alexflipnote.dev/
- **API base URL:** `https://coffee.alexflipnote.dev`

## Authentication

### No authentication

This public Coffee API does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://coffee.alexflipnote.dev/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 250 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Random Coffee Image](actions/get-random-coffee-image.md) | `GET /random` | [docs](https://coffee.alexflipnote.dev/) |
| [Get Random Coffee Image URL](actions/get-random-coffee-image-url.md) | `GET /random.json` | [docs](https://coffee.alexflipnote.dev/) |
