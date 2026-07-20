# <img src="https://images.mindcloud.co/apps/icons/mint-blue_1775149671545.jpeg" alt="mintBlue logo" width="28" height="28"> mintBlue: Universal API

mintBlue provides blockchain-backed data storage and automation APIs for transactions, projects, and event listeners.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mintBlue/latest
- **Category:** Content & Files / Storage
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mintblue.com
- **Vendor API docs:** https://mintblue.gitlab.io/sdk/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create Access Token](actions/create-access-token.md) | POST | Creates a new access token in mintBlue. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Listener](actions/create-event-listener.md) | POST | Creates a new event listener in mintBlue. |
| [Get Event Listener](actions/get-event-listener.md) | GET | Retrieves an event listener from mintBlue. |
| [List Event Listeners](actions/list-event-listeners.md) | GET | Retrieves event listeners from mintBlue. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in mintBlue. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes a project from mintBlue. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from mintBlue. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from mintBlue. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in mintBlue. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST | Creates a new transaction in mintBlue. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from mintBlue. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from mintBlue. |

