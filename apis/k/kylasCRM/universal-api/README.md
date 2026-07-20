# <img src="https://images.mindcloud.co/apps/icons/images-23_1774873316931.png" alt="Kylas CRM logo" width="28" height="28"> Kylas CRM: Universal API

Manage contacts, tasks, meetings, users, notes, pipelines, and CRM configuration in Kylas.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kylasCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kylas.io
- **Vendor API docs:** https://www.postman.com/kylasqa/kylas-apis/documentation/awdync1/kylas-apis-public

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Lead Duplicates](actions/check-lead-duplicates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/check-lead-duplicates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Kylas CRM. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Kylas CRM by ID. |
| [Get Contact Layout](actions/get-contact-layout.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Lookup Contacts](actions/lookup-contacts.md) | GET |  |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Kylas CRM by search filters. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Kylas CRM. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Deals](actions/lookup-deals.md) | GET |  |
| [Search Deals](actions/search-deals.md) | GET | Finds deals in Kylas CRM by search filters. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Check Lead Duplicates](actions/check-lead-duplicates.md) | GET |  |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Kylas CRM. |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes an existing lead from Kylas CRM. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Kylas CRM by ID. |
| [Get Lead Layout](actions/get-lead-layout.md) | GET | Retrieves lead form fields from Kylas CRM. |
| [Lookup Leads](actions/lookup-leads.md) | GET |  |
| [Search Leads](actions/search-leads.md) | GET | Finds leads in Kylas CRM by search filters. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Kylas CRM. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Create Layout](actions/get-task-create-layout.md) | GET | Retrieves task form fields from Kylas CRM. |
| [List Tasks](actions/list-tasks.md) | GET |  |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET |  |
| [Lookup Teams](actions/lookup-teams.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Currencies](actions/add-currencies.md) | POST |  |
| [List Active Currencies](actions/list-active-currencies.md) | GET |  |
| [List Fields](actions/list-fields.md) | GET |  |
| [Lookup Deal Pipelines](actions/lookup-deal-pipelines.md) | GET |  |
| [Lookup Lead Pipelines](actions/lookup-lead-pipelines.md) | GET |  |
| [Search Pipelines](actions/search-pipelines.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Kylas CRM by ID. |
| [List Users](actions/list-users.md) | GET |  |
| [Lookup Users](actions/lookup-users.md) | GET |  |
| [Search Users](actions/search-users.md) | GET |  |

