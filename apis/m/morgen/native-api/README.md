# Morgen: Native API Reference

A consolidated summary of Morgen's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.morgen.so/
- **API base URL:** `https://api.morgen.so`

## Authentication

### Morgen API Key

Use your Morgen API key with the provider-required Authorization header and store the default account and calendar IDs used for event operations.

### Credentials

- **API Key:** `apiKey` · required · Your Morgen API key.
- **Account ID:** `accountId` · required · Default Morgen account ID for calendar-scoped actions.
- **Calendar ID:** `calendarId` · required · Default writable Morgen calendar ID for event actions.

[Official authentication documentation](https://docs.morgen.so/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Close Task](actions/close-task.md) | `POST /v3/tasks/close` | [docs](https://docs.morgen.so/tasks#close-a-task) |
| [Create Event](actions/create-event.md) | `POST /v3/events/create` | [docs](https://docs.morgen.so/events#create-an-event) |
| [Create Task](actions/create-task.md) | `POST /v3/tasks/create` | [docs](https://docs.morgen.so/tasks#create-a-task) |
| [Delete Event](actions/delete-event.md) | `POST /v3/events/delete` | [docs](https://docs.morgen.so/events#delete-an-event) |
| [Delete Task](actions/delete-task.md) | `POST /v3/tasks/delete` | [docs](https://docs.morgen.so/tasks#delete-a-task) |
| [Get Task](actions/get-task.md) | `GET /v3/tasks` | [docs](https://docs.morgen.so/tasks#get-a-task) |
| [List Calendars](actions/list-calendars.md) | `GET /v3/calendars/list` | [docs](https://docs.morgen.so/calendars#list-calendars) |
| [List Events](actions/list-events.md) | `GET /v3/events/list` | [docs](https://docs.morgen.so/events#list-events) |
| [List Integration Accounts](actions/list-integration-accounts.md) | `GET /v3/integrations/accounts/list` | [docs](https://docs.morgen.so/integrations#how-to-list-the-connected-accounts-of-a-user) |
| [List Integrations](actions/list-integrations.md) | `GET /v3/integrations/list` | [docs](https://docs.morgen.so/integrations#how-to-list-the-available-providers) |
| [List Tasks](actions/list-tasks.md) | `GET /v3/tasks/list` | [docs](https://docs.morgen.so/tasks#list-tasks) |
| [Reopen Task](actions/reopen-task.md) | `POST /v3/tasks/reopen` | [docs](https://docs.morgen.so/tasks#reopen-a-task) |
| [Update Event](actions/update-event.md) | `POST /v3/events/update` | [docs](https://docs.morgen.so/events#update-an-event) |
| [Update Task](actions/update-task.md) | `POST /v3/tasks/update` | [docs](https://docs.morgen.so/tasks#update-a-task) |
