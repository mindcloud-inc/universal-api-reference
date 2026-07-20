# <img src="https://images.mindcloud.co/apps/icons/satiurn_1776355728333.png" alt="Satiurn logo" width="28" height="28"> Satiurn: Universal API

Manage contacts, proposals, projects, tasks, and finances

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/satiurn/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.satiurn.com/
- **Vendor API docs:** https://docs.satiurn.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Labels](actions/get-labels.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/get-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Create Board](actions/create-board.md) | POST | Creates a new board in Satiurn. |
| [Get Board](actions/get-board.md) | GET | Retrieves a board from Satiurn. |
| [Get Boards](actions/get-boards.md) | GET | Retrieves boards from Satiurn. |
| [Update Board](actions/update-board.md) | PUT | Updates an existing board in Satiurn. |

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar Entities](actions/get-calendar-entities.md) | GET | Retrieves calendar entities from Satiurn. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new finance category in Satiurn. |
| [Get Categories](actions/get-categories.md) | GET | Retrieves finance categories from Satiurn. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing finance category in Satiurn. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Resource](actions/create-resource.md) | POST | Creates a new resource in Satiurn. |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a resource from Satiurn. |
| [Get Resources](actions/get-resources.md) | GET | Retrieves resources from Satiurn. |
| [Update Resource](actions/update-resource.md) | PUT | Updates an existing resource in Satiurn. |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue in Satiurn. |
| [Get Issue](actions/get-issue.md) | GET | Retrieves an issue from Satiurn. |
| [Get Issues](actions/get-issues.md) | GET | Retrieves issues from Satiurn. |
| [Update Issue](actions/update-issue.md) | PUT | Updates an existing issue in Satiurn. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Create Label](actions/create-label.md) | POST | Creates a new label in Satiurn. |
| [Get Labels](actions/get-labels.md) | GET | Retrieves labels from Satiurn. |
| [Update Label](actions/update-label.md) | PUT | Updates an existing label in Satiurn. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Create Reminder](actions/create-reminder.md) | POST | Creates a new reminder in Satiurn. |
| [Get Reminder](actions/get-reminder.md) | GET | Retrieves a reminder from Satiurn. |
| [Update Reminder](actions/update-reminder.md) | PUT | Updates an existing reminder in Satiurn. |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [Create Pipeline](actions/create-pipeline.md) | POST | Creates a new pipeline in Satiurn. |
| [Get Pipelines](actions/get-pipelines.md) | GET | Retrieves pipelines from Satiurn. |
| [Update Pipeline](actions/update-pipeline.md) | PUT | Updates an existing pipeline in Satiurn. |

### Proposals

| Action | Method | Description |
| --- | --- | --- |
| [Create Proposal](actions/create-proposal.md) | POST | Creates a new proposal in Satiurn. |
| [Get Proposal](actions/get-proposal.md) | GET | Retrieves a proposal from Satiurn. |
| [Get Proposals](actions/get-proposals.md) | GET | Retrieves proposals from Satiurn. |
| [Update Proposal](actions/update-proposal.md) | PUT | Updates an existing proposal in Satiurn. |

### Stages

| Action | Method | Description |
| --- | --- | --- |
| [Create Stadium](actions/create-stadium.md) | POST | Creates a new stadium in Satiurn. |
| [Get Stadiums](actions/get-stadiums.md) | GET | Retrieves stadiums from Satiurn. |
| [Update Stadium](actions/update-stadium.md) | PUT | Updates an existing stadium in Satiurn. |

### Subtasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Subtask](actions/get-subtask.md) | GET | Retrieves a subtask from Satiurn. |
| [Get Subtasks](actions/get-subtasks.md) | GET | Retrieves subtasks from Satiurn. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Satiurn. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Satiurn. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Satiurn. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Movement](actions/create-movement.md) | POST | Creates a new financial movement in Satiurn. |
| [Get Movement](actions/get-movement.md) | GET | Retrieves a financial movement from Satiurn. |
| [Update Movement](actions/update-movement.md) | PUT | Updates an existing financial movement in Satiurn. |

