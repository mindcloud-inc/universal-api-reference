# <img src="https://images.mindcloud.co/apps/icons/intradesk_1776708761509.png" alt="Intradesk logo" width="28" height="28"> Intradesk: Universal API

Intradesk is an IT service management platform for service desk tickets, workflows, users, clients, assets, knowledge base content, and operational reporting.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/intradesk/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://intradesk.ru
- **Vendor API docs:** https://intradesk.ru/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset from Intradesk. |
| [List Assets](actions/list-assets.md) | GET | Retrieves assets from Intradesk. |
| [Search Assets](actions/search-assets.md) | GET | Finds assets in Intradesk by search text. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Get Task History Comment](actions/get-task-history-comment.md) | GET | Retrieves a task history comment from Intradesk. |
| [List Task History](actions/list-task-history.md) | GET | Retrieves task history entries from Intradesk. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Intradesk. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Intradesk. |
| [Search Clients](actions/search-clients.md) | GET | Finds clients in Intradesk by email or phone. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee](actions/get-employee.md) | GET | Retrieves an employee from Intradesk. |
| [List Employees](actions/list-employees.md) | GET | Retrieves employees from Intradesk. |
| [Search Employees](actions/search-employees.md) | GET | Finds employees in Intradesk by search text. |

### Expenses

| Action | Method | Description |
| --- | --- | --- |
| [List Task Expenses](actions/list-task-expenses.md) | GET | Retrieves task expenses from Intradesk. |
| [Log Task Expense](actions/log-task-expense.md) | POST | Logs a task expense in Intradesk. |

### Inventory Items

| Action | Method | Description |
| --- | --- | --- |
| [List Task Inventory](actions/list-task-inventory.md) | GET | Retrieves task inventory from Intradesk. |
| [Log Task Inventory](actions/log-task-inventory.md) | POST | Logs task inventory usage in Intradesk. |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [Get Knowledge Base Article](actions/get-knowledge-base-article.md) | GET | Retrieves a knowledge base article from Intradesk. |
| [List Knowledge Base Articles](actions/list-knowledge-base-articles.md) | GET | Retrieves knowledge base articles from Intradesk. |
| [Search Knowledge Base Articles](actions/search-knowledge-base-articles.md) | GET | Finds knowledge base articles in Intradesk by search text. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Accessible Services](actions/list-accessible-services.md) | GET | Retrieves accessible services from Intradesk. |
| [List Asset Services](actions/list-asset-services.md) | GET | Retrieves services with assets from Intradesk. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Task Statuses](actions/list-task-statuses.md) | GET | Retrieves task statuses from Intradesk. |
| [List Workflow Statuses](actions/list-workflow-statuses.md) | GET | Retrieves workflow statuses from Intradesk. |
| [List Workflow Transition Statuses](actions/list-workflow-transition-statuses.md) | GET | Retrieves workflow transition statuses from Intradesk. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Intradesk. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Intradesk. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Archive Task](actions/archive-task.md) | DELETE | Archives an existing task in Intradesk. |
| [Copy Task](actions/copy-task.md) | POST | Copies an existing task in Intradesk. |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Intradesk. |
| [Create Task Relation](actions/create-task-relation.md) | POST | Creates a task relation in Intradesk. |
| [Evaluate Task](actions/evaluate-task.md) | GET | Submits an evaluation for a task in Intradesk. |
| [List Dashboard Tickets](actions/list-dashboard-tickets.md) | GET | Retrieves dashboard tickets from Intradesk. |
| [List Task Relations](actions/list-task-relations.md) | GET | Retrieves task relations from Intradesk. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Intradesk. |
| [Set Task Active State](actions/set-task-active-state.md) | PUT | Sets a task's active state in Intradesk. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Intradesk. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Type Fields](actions/get-task-type-fields.md) | GET | Retrieves task type fields from Intradesk. |
| [List Priorities](actions/list-priorities.md) | GET | Retrieves priorities from Intradesk. |
| [List Task Types](actions/list-task-types.md) | GET | Retrieves task types from Intradesk. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Settings](actions/get-user-settings.md) | GET | Retrieves user settings from Intradesk. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from Intradesk. |

