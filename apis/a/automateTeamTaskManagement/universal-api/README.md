# <img src="https://images.mindcloud.co/apps/icons/automate-team-task-management_1776947895283.png" alt="Automate Team - Task Management logo" width="28" height="28"> Automate Team - Task Management: Universal API

Read Automate Team task workspaces, categories, users, and task records through the live Automate Business task data surfaces. This build is intentionally read-only because the provider's write surfaces remain tied to a different user-session contract that could not be validated with a tenant API key alone.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/automateTeamTaskManagement/latest
- **Category:** Productivity / Project Management
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.automatebusiness.com/products/task/
- **Vendor API docs:** https://developers.onautomate.com/task

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Task Counts](actions/get-task-counts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/get-task-counts?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Counts](actions/get-task-counts.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [List Task Users](actions/list-task-users.md) | GET |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Workspace](actions/lookup-workspace.md) | GET |  |

