# <img src="https://images.mindcloud.co/apps/icons/twenty_1773953665735.png" alt="Twenty logo" width="28" height="28"> Twenty: Universal API

Manage customer data, workflows, tasks, and dashboards in Twenty

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/twenty/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://twenty.com
- **Vendor API docs:** https://docs.twenty.com/developers/extend/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List People](actions/list-people.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [Delete Company](actions/delete-company.md) | DELETE |  |
| [Get Company](actions/get-company.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |
| [Update Company](actions/update-company.md) | PUT |  |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [Create Dashboard](actions/create-dashboard.md) | POST |  |
| [Delete Dashboard](actions/delete-dashboard.md) | DELETE |  |
| [Get Dashboard](actions/get-dashboard.md) | GET |  |
| [List Dashboards](actions/list-dashboards.md) | GET |  |
| [Update Dashboard](actions/update-dashboard.md) | PUT |  |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST |  |
| [Delete Note](actions/delete-note.md) | DELETE |  |
| [Get Note](actions/get-note.md) | GET |  |
| [List Notes](actions/list-notes.md) | GET |  |
| [Update Note](actions/update-note.md) | PUT |  |

### Object Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Create Object Metadata](actions/create-object-metadata.md) | POST |  |
| [Delete Object Metadata](actions/delete-object-metadata.md) | DELETE |  |
| [Get Object Metadata](actions/get-object-metadata.md) | GET |  |
| [List Object Metadata](actions/list-object-metadata.md) | GET |  |
| [Update Object Metadata](actions/update-object-metadata.md) | PUT |  |

### Opportunities

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity](actions/create-opportunity.md) | POST |  |
| [Delete Opportunity](actions/delete-opportunity.md) | DELETE |  |
| [Get Opportunity](actions/get-opportunity.md) | GET |  |
| [List Opportunities](actions/list-opportunities.md) | GET |  |
| [Update Opportunity](actions/update-opportunity.md) | PUT |  |

### People

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST |  |
| [Delete Person](actions/delete-person.md) | DELETE |  |
| [Get Person](actions/get-person.md) | GET |  |
| [List People](actions/list-people.md) | GET |  |
| [Update Person](actions/update-person.md) | PUT |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Delete Task](actions/delete-task.md) | DELETE |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST |  |
| [Delete Workflow](actions/delete-workflow.md) | DELETE |  |
| [Get Workflow](actions/get-workflow.md) | GET |  |
| [List Workflows](actions/list-workflows.md) | GET |  |
| [Update Workflow](actions/update-workflow.md) | PUT |  |

