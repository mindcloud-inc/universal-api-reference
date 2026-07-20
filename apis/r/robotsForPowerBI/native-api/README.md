# Robots for Power BI: Native API Reference

A consolidated summary of Robots for Power BI's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.pbirobots.powerbitiles.com/guides/api
- **OpenAPI specification:** https://www.powerbitiles.com/PBIRobots/docs/swagger/v1/swagger.json
- **API base URL:** `https://www.powerbitiles.com/PBIRobots`

## Authentication

### Account headers

Authenticate with the PowerBI Robots Account ID and Account Email headers required by the public API.

### Credentials

- **Account ID:** `accountId` · required · PowerBI Robots Account ID from Backoffice settings.
- **Account Email:** `accountEmail` · required · PowerBI Robots Account Email used with the Account ID.

Send these headers with each API request:

```http
AccountId: <accountId>
AccountEmail: <accountEmail>
```

[Official authentication documentation](https://docs.pbirobots.powerbitiles.com/guides/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Disable playlist](actions/disable-playlist.md) | `POST /api/v1/playlist.disable` | [docs](https://www.powerbitiles.com/PBIRobots/docs/swagger/index.html) |
| [Enable playlist](actions/enable-playlist.md) | `POST /api/v1/playlist.enable` | [docs](https://www.powerbitiles.com/PBIRobots/docs/swagger/index.html) |
| [Execute playlist](actions/execute-playlist.md) | `POST /api/v1/playlist.execute` | [docs](https://www.powerbitiles.com/PBIRobots/docs/swagger/index.html) |
