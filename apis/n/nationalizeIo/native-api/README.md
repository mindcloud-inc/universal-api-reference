# Nationalize_io: Native API Reference

A consolidated summary of Nationalize_io's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://nationalize.io/documentation
- **API base URL:** `https://api.nationalize.io`

## Authentication

### No authentication

Nationalize.io public prediction requests can be made without credentials for the no-auth usage tier.

This API does not require request authentication.

[Official authentication documentation](https://nationalize.io/documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Predict Nationalities for Names](actions/predict-nationalities-for-names.md) | `GET /` | [docs](https://nationalize.io/documentation) |
| [Predict Nationality by Name](actions/predict-nationality-by-name.md) | `GET /` | [docs](https://nationalize.io/documentation) |
