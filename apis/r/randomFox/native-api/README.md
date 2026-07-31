# RandomFox: Native API Reference

A consolidated summary of RandomFox's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://randomfox.ca/floof/
- **API base URL:** `https://randomfox.ca`

## Authentication

### No authentication

RandomFox public API requires no credentials.

This API does not require request authentication.

[Official authentication documentation](https://randomfox.ca/floof/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Random Fox](actions/get-random-fox.md) | `GET /floof/` | [docs](https://randomfox.ca/floof/) |
| [Get Random Foxes](actions/get-random-foxes.md) | `GET /api/v1/getfoxes/` | [docs](https://github.com/xinitrc-dev/randomfox.ca/blob/master/api/v1/getfoxes/index.php) |
