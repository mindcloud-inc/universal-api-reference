# <img src="https://images.mindcloud.co/apps/icons/moskit_1773939830404.png" alt="Moskit logo" width="28" height="28"> Moskit: Universal API

Manage contacts, companies, deals, projects, and sales activities

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moskit/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.moskitcrm.com
- **Vendor API docs:** https://moskit.stoplight.io/docs/api-v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moskit/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Moskit. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Moskit. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Moskit. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Moskit by search criteria. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Moskit. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Moskit. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Moskit. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Moskit. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Moskit by search criteria. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Moskit. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in Moskit. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a deal from Moskit. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deals from Moskit. |
| [Search Deals](actions/search-deals.md) | GET | Finds deals in Moskit by search criteria. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in Moskit. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Moskit. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Moskit. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Moskit. |
| [Search Projects](actions/search-projects.md) | GET | Finds projects in Moskit by search criteria. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Moskit. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity in Moskit. |
| [Get Activity](actions/get-activity.md) | GET | Retrieves an activity from Moskit. |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from Moskit. |
| [Search Activities](actions/search-activities.md) | GET | Finds activities in Moskit by search criteria. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an existing activity in Moskit. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Moskit. |

