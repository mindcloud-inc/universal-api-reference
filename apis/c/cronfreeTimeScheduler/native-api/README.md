# Cronfree Time Scheduler: Native API Reference

A consolidated summary of Cronfree Time Scheduler's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.cronfree.com/api
- **API base URL:** `https://login.cronfree.com/zapier`

## Authentication

### API Key

Use your Cronfree account License Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.cronfree.com/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | `POST /schedule` | [docs](https://docs.cronfree.com/api#subscribe-post) |
| [Delete Schedule](actions/delete-schedule.md) | `POST /unschedule` | [docs](https://docs.cronfree.com/api#unsubscribe) |
