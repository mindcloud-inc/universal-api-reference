# <img src="https://images.mindcloud.co/apps/icons/digiclose-icon_1782393207148.png" alt="Digiclose logo" width="28" height="28"> Digiclose: Universal API

Manage contacts, pipelines, tasks, and deals in Digiclose

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/digiclose/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://digiclose.ai
- **Vendor API docs:** https://app.digiclose.ai/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Contact Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Field Definitions](actions/get-contact-field-definitions.md) | GET |  |

### Contact Notice

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Notices](actions/list-contact-notices.md) | GET |  |

### Deal Phase

| Action | Method | Description |
| --- | --- | --- |
| [List Pipeline Deal Phases](actions/list-pipeline-deal-phases.md) | GET |  |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline](actions/get-pipeline.md) | GET |  |
| [List Pipelines](actions/list-pipelines.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Get Product](actions/get-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |
| [List Recent Products](actions/list-recent-products.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Contact Tasks](actions/list-contact-tasks.md) | GET |  |
| [List Recent Tasks](actions/list-recent-tasks.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |

### Task Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Category](actions/create-task-category.md) | POST |  |
| [List Task Categories](actions/list-task-categories.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST |  |
| [Get Team](actions/get-team.md) | GET |  |
| [List Teams](actions/list-teams.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |

