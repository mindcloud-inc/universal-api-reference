# mintBlue: Native API Reference

A consolidated summary of mintBlue's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://mintblue.gitlab.io/sdk/
- **API base URL:** `https://api.mintblue.com`

## Authentication

### SDK Token

Authenticate requests with the mintBlue SDK token passed in the mintblue-sdk-token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
mintblue-sdk-token: <apiKey>
```

[Official authentication documentation](https://docs.mintblue.com/quick-start)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `result`.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Access Token](actions/create-access-token.md) | `POST /sdk/latest` | [docs](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#createAccesstoken) |
| [Create Event Listener](actions/create-event-listener.md) | `POST /sdk/latest` | [docs](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#createEventListener) |
| [Create Project](actions/create-project.md) | `POST /sdk/latest` | [docs](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#createProject) |
| [Create Transaction](actions/create-transaction.md) | `POST /sdk/latest` | [docs](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#createTransaction) |
| [Delete Project](actions/delete-project.md) | `POST /sdk/latest` | [docs](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#destroyProject) |
| [Get Event Listener](actions/get-event-listener.md) | `POST /sdk/latest` | [docs](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#getEventListener) |
| [Get Project](actions/get-project.md) | `POST /sdk/latest` | [docs](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#getProject) |
| [Get Transaction](actions/get-transaction.md) | `POST /sdk/latest` | [docs](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#getTransaction) |
| [List Event Listeners](actions/list-event-listeners.md) | `POST /sdk/latest` | [docs](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#listEventListeners) |
| [List Projects](actions/list-projects.md) | `POST /sdk/latest` | [docs](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#listProjects) |
| [List Transactions](actions/list-transactions.md) | `POST /sdk/latest` | [docs](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#listTransactions) |
| [Update Project](actions/update-project.md) | `POST /sdk/latest` | [docs](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#updateProject) |
