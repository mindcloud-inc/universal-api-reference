# <img src="https://images.mindcloud.co/apps/icons/apps_1775232873503.png" alt="Zoho Sprints logo" width="28" height="28"> Zoho Sprints: Universal API

Manage Zoho Sprints workspaces, projects, sprints, items, comments, attachments, and workflow status through the official Zoho Sprints API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoSprints/latest
- **Category:** Support / Ticketing
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sprints.zoho.com/
- **Vendor API docs:** https://sprints.zoho.com/apidoc.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Add Item Attachments](actions/add-item-attachments.md) | POST | Adds attachments to an item in Zoho Sprints. |

### Item Type

| Action | Method | Description |
| --- | --- | --- |
| [List Item Types](actions/list-item-types.md) | GET | Retrieves item types from Zoho Sprints. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST | Creates a new item in Zoho Sprints. |
| [Get Item Details](actions/get-item-details.md) | GET | Retrieves item details from Zoho Sprints. |
| [List Items](actions/list-items.md) | GET | Retrieves items from Zoho Sprints. |
| [Move Item](actions/move-item.md) | PUT | Moves items to another sprint in Zoho Sprints. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in Zoho Sprints. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Zoho Sprints. |
| [Get Project Backlog](actions/get-project-backlog.md) | GET | Retrieves a project backlog from Zoho Sprints. |
| [Get Project Details](actions/get-project-details.md) | GET | Retrieves project details from Zoho Sprints. |
| [Get Project Status](actions/get-project-status.md) | GET | Retrieves project item statuses from Zoho Sprints. |
| [List Project Priorities](actions/list-project-priorities.md) | GET | Retrieves project priorities from Zoho Sprints. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Zoho Sprints. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Zoho Sprints. |

### Sprint

| Action | Method | Description |
| --- | --- | --- |
| [Complete Sprint](actions/complete-sprint.md) | PUT | Completes an existing sprint in Zoho Sprints. |
| [Create Sprint](actions/create-sprint.md) | POST | Creates a new sprint in Zoho Sprints. |
| [Get Sprint Details](actions/get-sprint-details.md) | GET | Retrieves sprint details from Zoho Sprints. |
| [List Sprints](actions/list-sprints.md) | GET | Retrieves sprints from Zoho Sprints. |
| [Start Sprint](actions/start-sprint.md) | PUT | Starts an existing sprint in Zoho Sprints. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Zoho Sprints. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Users](actions/list-workspace-users.md) | GET | Retrieves workspace users from Zoho Sprints. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Settings](actions/get-workspace-settings.md) | GET | Retrieves workspace settings from Zoho Sprints. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Zoho Sprints. |

