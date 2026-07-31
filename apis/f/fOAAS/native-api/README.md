# FOAAS: Native API Reference

A consolidated summary of FOAAS's API configuration and 5 documented operations.

- **API base URL:** `https://foaas.io`

## Authentication

### No authentication

This API does not require request authentication.

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Asshole](actions/asshole.md) | `GET /asshole/:from` | [docs](https://foaas.io/) |
| [Back Off](actions/back-off.md) | `GET /back/:name/:from` | [docs](https://foaas.io/) |
| [Get Version](actions/get-version.md) | `GET /version` | [docs](https://foaas.io/) |
| [List Operations](actions/list-operations.md) | `GET /operations` | [docs](https://foaas.io/) |
| [Random Message](actions/random-message.md) | `GET /random/:from` | [docs](https://foaas.io/) |
