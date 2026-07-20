# <img src="https://images.mindcloud.co/apps/icons/blue_1775253730172.png" alt="Blue logo" width="28" height="28"> Blue: Universal API

Manage workspaces, records, lists, comments, documents, and automations in Blue.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blue/latest
- **Category:** Productivity / Project Management
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://blue.cc/
- **Vendor API docs:** https://blue.cc/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blue/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Blue by ID. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from your Blue account. |

### Company Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Company Invoices](actions/list-company-invoices.md) | GET | Retrieves invoices for a Blue company. |

### Company User

| Action | Method | Description |
| --- | --- | --- |
| [List Company Users](actions/list-company-users.md) | GET | Retrieves users for a Blue company. |

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [List Dashboards](actions/list-dashboards.md) | GET | Retrieves dashboards from a Blue company. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Project Folders](actions/list-project-folders.md) | GET | Retrieves project folders from a Blue company. |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [List My Invitations](actions/list-my-invitations.md) | GET | Retrieves your pending invitations from Blue. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [List Links](actions/list-links.md) | GET | Retrieves links from a Blue company. |

### Notification Option

| Action | Method | Description |
| --- | --- | --- |
| [List Notification Options](actions/list-notification-options.md) | GET | Retrieves available notification options from Blue. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Blue. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Blue. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects for a Blue company. |
| [List Recent Projects](actions/list-recent-projects.md) | GET | Retrieves recent projects from Blue. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Blue. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from a Blue company. |

### Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Stats](actions/get-stats.md) | GET | Retrieves account summary stats from Blue. |

### Subscription Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Available Subscription Plans](actions/list-available-subscription-plans.md) | GET | Retrieves available subscription plans from Blue. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Blue. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Blue by ID. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves configured webhooks from Blue. |

