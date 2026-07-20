# <img src="https://images.mindcloud.co/apps/icons/favicon-api-docs-platrum-ru-48x48_1776946990530.png" alt="Platrum logo" width="28" height="28"> Platrum: Universal API

Platrum is a company management platform for company structure, tasks, knowledge base, finance, training, password storage, and internal operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/platrum/latest
- **Category:** Productivity / Project Management
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://platrum.com
- **Vendor API docs:** http://api.docs.platrum.ru

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List profiles](actions/list-profiles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platrum/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List cashboxes](actions/list-cashboxes.md) | GET | Retrieves cashboxes from Platrum. |

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Delete board](actions/delete-board.md) | DELETE | Deletes a board from Platrum. |
| [List task boards](actions/list-task-boards.md) | GET | Retrieves task boards from Platrum. |
| [Save board](actions/save-board.md) | POST | Creates or updates a board in Platrum. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List finance categories](actions/list-finance-categories.md) | GET | Retrieves finance transaction types from Platrum. |
| [List item categories](actions/list-item-categories.md) | GET | Retrieves store item categories from Platrum. |
| [List password categories](actions/list-password-categories.md) | GET | Retrieves password categories from Platrum. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Save counterparty](actions/save-counterparty.md) | POST | Creates or updates a counterparty in Platrum. |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [List org blocks](actions/list-org-blocks.md) | GET | Retrieves organization blocks from Platrum. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [List active workers](actions/list-active-workers.md) | GET | Retrieves active worker positions from Platrum. |
| [List staff](actions/list-staff.md) | GET | Retrieves staff members from Platrum. |
| [List workers](actions/list-workers.md) | GET | Retrieves all worker positions from Platrum. |

### Exchange Rates

| Action | Method | Description |
| --- | --- | --- |
| [Get exchange rate](actions/get-exchange-rate.md) | GET | Retrieves a Platrum currency exchange rate by date. |

### Expenses

| Action | Method | Description |
| --- | --- | --- |
| [List budget requests](actions/list-budget-requests.md) | GET | Retrieves budget requests from Platrum. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Archive space](actions/archive-space.md) | DELETE | Archives a knowledge space in Platrum and deletes its articles. |
| [List spaces](actions/list-spaces.md) | GET | Retrieves knowledge spaces from Platrum. |
| [Save space](actions/save-space.md) | POST | Creates or updates a knowledge space in Platrum. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List store items](actions/list-store-items.md) | GET | Retrieves store items from Platrum. |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [Delete article](actions/delete-article.md) | DELETE | Deletes a knowledge article from Platrum. |
| [Get article](actions/get-article.md) | GET | Retrieves a knowledge article from Platrum by ID. |
| [List articles](actions/list-articles.md) | GET | Retrieves knowledge articles from Platrum. |
| [Save article](actions/save-article.md) | POST | Creates or updates a knowledge article in Platrum. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List active currencies](actions/list-active-currencies.md) | GET | Retrieves active currencies from Platrum. |
| [List currencies](actions/list-currencies.md) | GET | Retrieves currencies from Platrum. |

### Programs

| Action | Method | Description |
| --- | --- | --- |
| [List courses](actions/list-courses.md) | GET | Retrieves courses from Platrum. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List schedules](actions/list-schedules.md) | GET | Retrieves work schedules from Platrum. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [List passwords](actions/list-passwords.md) | GET | Retrieves passwords from Platrum. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create task](actions/create-task.md) | POST | Creates a new task in Platrum. |
| [Get task](actions/get-task.md) | GET | Retrieves a task from Platrum by ID. |
| [List board tasks](actions/list-board-tasks.md) | GET | Retrieves tasks from a Platrum board. |
| [List tasks](actions/list-tasks.md) | GET | Finds tasks in Platrum by filter. |
| [Remove task](actions/remove-task.md) | DELETE | Deletes a task from Platrum. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List profiles](actions/list-profiles.md) | GET | Retrieves profiles from Platrum. |

