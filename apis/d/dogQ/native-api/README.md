# DogQ: Native API Reference

A consolidated summary of DogQ's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.dogq.io/documentation/integrations
- **API base URL:** `https://dogq.io`

## Authentication

### Project Token

Connect DogQ with a project token from the project settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Token: <apiKey>
```

[Official authentication documentation](https://docs.dogq.io/documentation/integrations/zapier/dogq-zapier-integration-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Run Project](actions/run-project.md) | `POST /projects/external_execute` | [docs](https://docs.dogq.io/documentation/integrations/ci-cd) |
