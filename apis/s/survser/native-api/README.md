# Survser: Native API Reference

A consolidated summary of Survser's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.survser.com/docs/api
- **API base URL:** `https://survser.com/api/public/`

## Authentication

### API Key

Survser public API key passed as the `key` query parameter.

### Credentials

- **API Key:** `apiKey` · required · Survser public API key. The public API expects this value in the `key` query parameter.

[Official authentication documentation](https://docs.survser.com/docs/api)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Survey Responses](actions/list-survey-responses.md) | `GET /response/list` | [docs](https://docs.survser.com/docs/api) |
| [List Surveys](actions/list-surveys.md) | `GET /survey/list` | [docs](https://docs.survser.com/docs/api) |
