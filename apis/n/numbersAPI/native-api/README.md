# Numbers API: Native API Reference

A consolidated summary of Numbers API's API configuration and 5 documented operations.

- **API base URL:** `http://numbersapi.com`

## Authentication

### No authentication

This API does not require request authentication.

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Date Fact](actions/get-date-fact.md) | `GET /:month/:day/date` | [docs](http://numbersapi.com/#api) |
| [Get Number Math Fact](actions/get-number-math-fact.md) | `GET /:number/math` | [docs](http://numbersapi.com/#api) |
| [Get Number Trivia](actions/get-number-trivia.md) | `GET /:number/trivia` | [docs](http://numbersapi.com/#api) |
| [Get Random Fact](actions/get-random-fact.md) | `GET /random/:type` | [docs](http://numbersapi.com/#api) |
| [Get Year Fact](actions/get-year-fact.md) | `GET /:year/year` | [docs](http://numbersapi.com/#api) |
