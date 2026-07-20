# <img src="https://images.mindcloud.co/apps/icons/uspacy_1774560460261.png" alt="Uspacy logo" width="28" height="28"> Uspacy: Universal API

Manage CRM, tasks, webhooks, and team activity in Uspacy

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uspacy/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://uspacy.com
- **Vendor API docs:** https://uspacy.readme.io/reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Self Profile](actions/get-self-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/get-self-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity in Uspacy. |
| [List Activities](actions/list-activities.md) | GET | Retrieves all activity records from Uspacy. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Uspacy. |
| [List Comments](actions/list-comments.md) | GET | Retrieves all comment records from Uspacy. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Retrieves all company records from Uspacy. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves all contact records from Uspacy. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [List CRM Entities](actions/list-crm-entities.md) | GET | Retrieves available CRM entity types from Uspacy. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [List Deals](actions/list-deals.md) | GET | Retrieves all deal records from Uspacy. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create CRM Entity Item](actions/create-crm-entity-item.md) | POST | Creates a new CRM entity item in Uspacy. |
| [Get CRM Entity Item](actions/get-crm-entity-item.md) | GET | Retrieves a CRM entity item from Uspacy. |
| [List CRM Entity Items](actions/list-crm-entity-items.md) | GET | Retrieves CRM entity items from Uspacy. |
| [Search Workspace Data](actions/search-workspace-data.md) | GET | Finds matching workspace data in Uspacy. |
| [Update CRM Entity Item](actions/update-crm-entity-item.md) | PUT | Updates an existing CRM entity item in Uspacy. |

### Stages

| Action | Method | Description |
| --- | --- | --- |
| [List Task Stages](actions/list-task-stages.md) | GET | Retrieves task stage records from Uspacy. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Uspacy. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task record from Uspacy. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves all task records from Uspacy. |
| [Move Task To Stage](actions/move-task-to-stage.md) | PUT | Moves a task to a Uspacy stage. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Uspacy. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Self Profile](actions/get-self-profile.md) | GET | Retrieves the authenticated user profile from Uspacy. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves all workspace users from Uspacy. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Outgoing Webhook](actions/create-outgoing-webhook.md) | POST | Creates a new outgoing webhook in Uspacy. |
| [List Outgoing Webhooks](actions/list-outgoing-webhooks.md) | GET | Retrieves outgoing webhook entries from Uspacy. |
| [Toggle Outgoing Webhook Status](actions/toggle-outgoing-webhook-status.md) | PUT | Updates an outgoing webhook status in Uspacy. |

