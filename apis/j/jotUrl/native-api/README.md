# JotUrl: Native API Reference

A consolidated summary of JotUrl's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://i1.joturl.com/
- **API base URL:** `https://joturl.com/a/i1`

## Authentication

### Bearer Token

Use a JotUrl bearer token generated from the provider's token authentication flow.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://i1.joturl.com/#token-authentication)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Conversion Codes](actions/count-conversion-codes.md) | `GET /conversions/codes/count` | [docs](https://i1.joturl.com/#conversions-codes-count) |
| [Count Domains](actions/count-domains.md) | `GET /domains/count` | [docs](https://i1.joturl.com/#domains-count) |
| [Count Projects](actions/count-projects.md) | `GET /projects/count` | [docs](https://i1.joturl.com/#projects-count) |
| [Count URLs](actions/count-urls.md) | `GET /urls/count` | [docs](https://i1.joturl.com/#urls-count) |
| [Create Conversion Code](actions/create-conversion-code.md) | `POST /conversions/codes/add` | [docs](https://i1.joturl.com/#conversions-codes-add) |
| [Create Domain](actions/create-domain.md) | `POST /domains/add` | [docs](https://i1.joturl.com/#domains-add) |
| [Create Project](actions/create-project.md) | `POST /projects/add` | [docs](https://i1.joturl.com/#projects-add) |
| [Create Watchdog](actions/create-watchdog.md) | `POST /watchdogs/add` | [docs](https://i1.joturl.com/#watchdogs-add) |
| [Delete Conversion Code](actions/delete-conversion-code.md) | `POST /conversions/codes/delete` | [docs](https://i1.joturl.com/#conversions-codes-delete) |
| [Delete Domain](actions/delete-domain.md) | `POST /domains/delete` | [docs](https://i1.joturl.com/#domains-delete) |
| [Delete Project](actions/delete-project.md) | `POST /projects/delete` | [docs](https://i1.joturl.com/#projects-delete) |
| [Delete URL](actions/delete-url.md) | `POST /urls/delete` | [docs](https://i1.joturl.com/#urls-delete) |
| [Delete Watchdog](actions/delete-watchdog.md) | `POST /watchdogs/delete` | [docs](https://i1.joturl.com/#watchdogs-delete) |
| [Get Conversion Code](actions/get-conversion-code.md) | `GET /conversions/codes/info` | [docs](https://i1.joturl.com/#conversions-codes-info) |
| [Get Domain](actions/get-domain.md) | `GET /domains/info` | [docs](https://i1.joturl.com/#domains-info) |
| [Get Last URL](actions/get-last-url.md) | `GET /urls/last` | [docs](https://i1.joturl.com/#urls-last) |
| [Get Project](actions/get-project.md) | `GET /projects/info` | [docs](https://i1.joturl.com/#projects-info) |
| [Get URL](actions/get-url.md) | `GET /urls/info` | [docs](https://i1.joturl.com/#urls-info) |
| [Get Watchdog](actions/get-watchdog.md) | `GET /watchdogs/info` | [docs](https://i1.joturl.com/#watchdogs-info) |
| [Get Watchdog Stats](actions/get-watchdog-stats.md) | `GET /watchdogs/stats` | [docs](https://i1.joturl.com/#watchdogs-stats) |
| [List Conversion Codes](actions/list-conversion-codes.md) | `GET /conversions/codes/list` | [docs](https://i1.joturl.com/#conversions-codes-list) |
| [List Domains](actions/list-domains.md) | `GET /domains/list` | [docs](https://i1.joturl.com/#domains-list) |
| [List Projects](actions/list-projects.md) | `GET /projects/list` | [docs](https://i1.joturl.com/#projects-list) |
| [List URLs](actions/list-urls.md) | `GET /urls/list` | [docs](https://i1.joturl.com/#urls-list) |
| [Shorten URL](actions/shorten-url.md) | `POST /urls/shorten` | [docs](https://i1.joturl.com/#urls-shorten) |
| [Suggest URL Alias](actions/suggest-url-alias.md) | `GET /urls/suggest` | [docs](https://i1.joturl.com/#urls-suggest) |
| [Update Conversion Code](actions/update-conversion-code.md) | `POST /conversions/codes/edit` | [docs](https://i1.joturl.com/#conversions-codes-edit) |
| [Update Domain](actions/update-domain.md) | `POST /domains/edit` | [docs](https://i1.joturl.com/#domains-edit) |
| [Update Project](actions/update-project.md) | `POST /projects/edit` | [docs](https://i1.joturl.com/#projects-edit) |
| [Update URL](actions/update-url.md) | `POST /urls/edit` | [docs](https://i1.joturl.com/#urls-edit) |
