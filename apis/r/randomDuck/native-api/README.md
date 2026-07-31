# Random Duck: Native API Reference

A consolidated summary of Random Duck's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://random-d.uk/api
- **API base URL:** `https://random-d.uk/api/v2`

## Authentication

### No authentication

Random Duck's public V2 read endpoints do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://random-d.uk/api)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Duck GIF by Number](actions/get-duck-gif-by-number.md) | `GET /:num.gif` | [docs](https://random-d.uk/api) |
| [Get Duck Image by Number](actions/get-duck-image-by-number.md) | `GET /:num.jpg` | [docs](https://random-d.uk/api) |
| [Get HTTP Status Duck](actions/get-http-status-duck.md) | `GET /http/:code` | [docs](https://random-d.uk/api) |
| [Get Random Duck](actions/get-random-duck.md) | `GET /random` | [docs](https://random-d.uk/api) |
| [Get Random Duck Image](actions/get-random-duck-image.md) | `GET /randomimg` | [docs](https://random-d.uk/api) |
| [Get Random Duck (Quack)](actions/get-random-duck-quack.md) | `GET /quack` | [docs](https://random-d.uk/api) |
| [List Available Ducks](actions/list-available-ducks.md) | `GET /list` | [docs](https://random-d.uk/api) |
