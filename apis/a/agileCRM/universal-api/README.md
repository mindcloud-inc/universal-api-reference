# <img src="https://images.mindcloud.co/apps/icons/agile-crm_1771963638996.png" alt="Agile CRM logo" width="28" height="28"> Agile CRM: Universal API

Manage contacts, track deals, automate marketing, and support customers.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agileCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.agilecrm.com
- **Vendor API docs:** https://github.com/agilecrm/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Agile CRM. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from Agile CRM. |
| [List Companies](actions/list-companies.md) | GET | Finds companies in Agile CRM by filters. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Agile CRM. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Agile CRM. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Agile CRM. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Agile CRM by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Finds contacts in Agile CRM by filters. |
| [Search Contacts and Companies](actions/search-contacts-and-companies.md) | GET | Finds contacts and companies in Agile CRM. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Agile CRM. |
| [Update Contact Tags](actions/update-contact-tags.md) | PUT | Updates tags for a contact in Agile CRM. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in Agile CRM. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes an existing deal from Agile CRM. |
| [List Deals](actions/list-deals.md) | GET | Finds deals in Agile CRM by filters. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in Agile CRM. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in Agile CRM. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Agile CRM. |

