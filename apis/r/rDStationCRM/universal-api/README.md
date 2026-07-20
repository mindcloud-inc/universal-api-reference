# <img src="https://images.mindcloud.co/apps/icons/62449537809bb9263d1cdacc-logo2_1773241220600.png" alt="RD Station CRM logo" width="28" height="28"> RD Station CRM: Universal API

Manage RD Station CRM contacts, deals, organizations, tasks, and users

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rDStationCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rdstation.com/produtos/crm/
- **Vendor API docs:** https://developers.rdstation.com/reference/crm-v2-introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in RD Station CRM. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves contact details from RD Station CRM. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from RD Station CRM. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in RD Station CRM. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in RD Station CRM. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves deal details from RD Station CRM. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deals from RD Station CRM. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in RD Station CRM. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates a new organization in RD Station CRM. |
| [Get Organization](actions/get-organization.md) | GET | Retrieves organization details from RD Station CRM. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from RD Station CRM. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in RD Station CRM. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline](actions/get-pipeline.md) | GET | Retrieves sales pipeline details from RD Station CRM. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves sales pipelines from RD Station CRM. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Get Source](actions/get-source.md) | GET | Retrieves a deal source from RD Station CRM. |
| [List Sources](actions/list-sources.md) | GET | Retrieves deal sources from RD Station CRM. |

### Stage

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline Stage](actions/get-pipeline-stage.md) | GET | Retrieves a sales pipeline stage from RD Station CRM. |
| [List Pipeline Stages](actions/list-pipeline-stages.md) | GET | Retrieves stages from a sales pipeline in RD Station CRM. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in RD Station CRM. |
| [Get Task](actions/get-task.md) | GET | Retrieves task details from RD Station CRM. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from RD Station CRM. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in RD Station CRM. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves user details from RD Station CRM. |
| [List Users](actions/list-users.md) | GET | Retrieves users from RD Station CRM. |

