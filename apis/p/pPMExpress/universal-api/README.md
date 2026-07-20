# <img src="https://images.mindcloud.co/apps/icons/p-pmexpress_1774983251540.png" alt="PPM Express logo" width="28" height="28"> PPM Express: Universal API

PPM Express is an online project portfolio management platform. This app wraps the documented PPM Express Public API for projects, ideas, challenges, tasks, key dates, resources, and related portfolio-management entities.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pPMExpress/latest
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ppm.express
- **Vendor API docs:** https://help.ppm.express/public-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Administrative Category

| Action | Method | Description |
| --- | --- | --- |
| [List Administrative Categories](actions/list-administrative-categories.md) | GET |  |

### Calendar Exception

| Action | Method | Description |
| --- | --- | --- |
| [List Global Calendar Exceptions](actions/list-global-calendar-exceptions.md) | GET |  |

### Challenge

| Action | Method | Description |
| --- | --- | --- |
| [Get Challenge](actions/get-challenge.md) | GET |  |
| [List Challenges](actions/list-challenges.md) | GET |  |

### Challenge Field

| Action | Method | Description |
| --- | --- | --- |
| [List Challenge Fields](actions/list-challenge-fields.md) | GET |  |

### Deliverable

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Deliverable](actions/get-project-deliverable.md) | GET |  |
| [List Project Deliverables](actions/list-project-deliverables.md) | GET |  |

### Idea

| Action | Method | Description |
| --- | --- | --- |
| [Get Idea](actions/get-idea.md) | GET |  |
| [List Ideas](actions/list-ideas.md) | GET |  |

### Idea Field

| Action | Method | Description |
| --- | --- | --- |
| [List Idea Fields](actions/list-idea-fields.md) | GET |  |

### Key Date

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Key Date](actions/get-project-key-date.md) | GET |  |
| [List Project Key Dates](actions/list-project-key-dates.md) | GET |  |

### Key Date Field

| Action | Method | Description |
| --- | --- | --- |
| [List Key Date Fields](actions/list-key-date-fields.md) | GET |  |

### Portfolio

| Action | Method | Description |
| --- | --- | --- |
| [Get Portfolio](actions/get-portfolio.md) | GET |  |
| [List Portfolios](actions/list-portfolios.md) | GET |  |

### Portfolio Field

| Action | Method | Description |
| --- | --- | --- |
| [List Portfolio Fields](actions/list-portfolio-fields.md) | GET |  |

### Program

| Action | Method | Description |
| --- | --- | --- |
| [Get Program](actions/get-program.md) | GET |  |
| [List Programs](actions/list-programs.md) | GET |  |

### Program Field

| Action | Method | Description |
| --- | --- | --- |
| [List Program Fields](actions/list-program-fields.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Project Field

| Action | Method | Description |
| --- | --- | --- |
| [List Project Fields](actions/list-project-fields.md) | GET |  |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource](actions/get-resource.md) | GET |  |
| [List Resources](actions/list-resources.md) | GET |  |

### Resource Calendar Exception

| Action | Method | Description |
| --- | --- | --- |
| [List Resource Calendar Exceptions](actions/list-resource-calendar-exceptions.md) | GET |  |

### Resource Field

| Action | Method | Description |
| --- | --- | --- |
| [List Resource Fields](actions/list-resource-fields.md) | GET |  |

### Resource Work Week Hours

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Work Week Hours](actions/get-resource-work-week-hours.md) | GET |  |

### Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Settings](actions/get-settings.md) | GET |  |

### Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Project Process Stages](actions/list-project-process-stages.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List Project Tasks](actions/list-project-tasks.md) | GET |  |

### Task Field

| Action | Method | Description |
| --- | --- | --- |
| [List Task Fields](actions/list-task-fields.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Task](actions/get-project-task.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

### Work Week Hours

| Action | Method | Description |
| --- | --- | --- |
| [Get Global Work Week Hours](actions/get-global-work-week-hours.md) | GET |  |

