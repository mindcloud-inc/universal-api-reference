# VosFactures: Native API Reference

A consolidated summary of VosFactures's API configuration, with links to official documentation.

- **Official docs:** https://app.vosfactures.fr/api
- **API base URL:** `https://mindcloudvosfactures.vosfactures.fr`

## Authentication

### API Key

Use your VosFactures API token from Paramètres du compte > Intégration > Code d'autorisation API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://mindcloudvosfactures.vosfactures.fr/api_tokens)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order` in the query string. Only one sort field is accepted.
