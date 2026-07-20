# Syften: Native API Reference

A consolidated summary of Syften's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://github.com/syften/syften-examples
- **API base URL:** `https://syften.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://syften.com/documentation)

## API conventions

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Info](actions/get-info.md) | `POST /api/0.0/info/get` | [docs](https://github.com/syften/syften-examples/blob/master/curl/info_get.sh) |
| [Get Settings](actions/get-settings.md) | `POST /api/0.0/settings/get` | [docs](https://github.com/syften/syften-examples/blob/master/curl/settings_get.sh) |
| [List Filters](actions/list-filters.md) | `POST /api/0.0/filters/get` | [docs](https://github.com/syften/syften-examples/blob/master/curl/filters_get.sh) |
| [List Items](actions/list-items.md) | `POST /api/0.0/items/get` | [docs](https://github.com/syften/syften-examples/blob/master/curl/items_get.sh) |
| [Set Filters](actions/set-filters.md) | `POST /api/0.0/filters/set` | [docs](https://github.com/syften/syften-examples/blob/master/curl/filters_set.sh) |
