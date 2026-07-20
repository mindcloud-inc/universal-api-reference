# Botmother: Native API Reference

A consolidated summary of Botmother's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.botmother.com/article/42097
- **API base URL:** `{eventUrl}`

## Authentication

### Botmother External Event URL

Use a Botmother External Event URL generated from Settings -> Events for the target bot event.

### Credentials

- **Event URL:** `eventUrl` · required · Full Botmother External Event URL generated for the target bot event.

[Official authentication documentation](https://docs.botmother.com/article/42097)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Trigger External Event For Botmother Users](actions/trigger-external-event-for-botmother-users.md) | `POST /` | [docs](https://docs.botmother.com/article/42097#bm_id) |
| [Trigger External Event For Botmother Users And Close Dialogs](actions/trigger-external-event-for-botmother-users-and-close-dialogs.md) | `POST /` | [docs](https://docs.botmother.com/article/42097#chat) |
| [Trigger External Event For Everyone](actions/trigger-external-event-for-everyone.md) | `POST /` | [docs](https://docs.botmother.com/article/42097#request) |
| [Trigger External Event For Everyone And Close Dialogs](actions/trigger-external-event-for-everyone-and-close-dialogs.md) | `POST /` | [docs](https://docs.botmother.com/article/42097#chat) |
| [Trigger External Event For Platform Users](actions/trigger-external-event-for-platform-users.md) | `POST /` | [docs](https://docs.botmother.com/article/42097#request) |
| [Trigger External Event For Platform Users And Close Dialogs](actions/trigger-external-event-for-platform-users-and-close-dialogs.md) | `POST /` | [docs](https://docs.botmother.com/article/42097#chat) |
