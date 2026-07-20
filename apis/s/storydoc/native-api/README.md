# Storydoc: Native API Reference

A consolidated summary of Storydoc's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://docs.storydoc.com/
- **OpenAPI specification:** https://docs.storydoc.com/source.json
- **API base URL:** `https://api.storydoc.com`

## Authentication

### API Key

Use your Storydoc Automations API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.storydoc.com/source.json)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Story Version](actions/create-story-version.md) | `POST /v2/versions` | [docs](https://docs.storydoc.com/operation/operation-createstoryversion) |
| [Get Account Details](actions/get-account-details.md) | `GET /v2/account` | [docs](https://docs.storydoc.com/operation/operation-getaccount) |
| [Get Story Details](actions/get-story-details.md) | `GET /v2/stories/:storyId` | [docs](https://docs.storydoc.com/operation/operation-getstory) |
| [List Stories](actions/list-stories.md) | `GET /v2/stories` | [docs](https://docs.storydoc.com/operation/operation-getstories) |
