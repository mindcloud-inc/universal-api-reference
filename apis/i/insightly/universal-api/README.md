# <img src="https://images.mindcloud.co/apps/icons/insightly_1773332541177.png" alt="Insightly logo" width="28" height="28"> Insightly: Universal API

Insightly: Manage CRM contacts, leads, organizations, opportunities, projects, and tasks through the official Insightly CRM API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/insightly/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.insightly.com/
- **Vendor API docs:** https://api.insightly.com/v3.1/Help

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Insightly. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Insightly by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Insightly. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Insightly by search filters. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Insightly. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Insightly. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Insightly by ID. |
| [List Leads](actions/list-leads.md) | GET | Retrieves a list of leads from Insightly. |
| [Search Leads](actions/search-leads.md) | GET | Finds leads in Insightly by search filters. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Insightly. |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity](actions/create-opportunity.md) | POST | Creates a new opportunity in Insightly. |
| [Get Opportunity](actions/get-opportunity.md) | GET | Retrieves an opportunity from Insightly by ID. |
| [List Opportunities](actions/list-opportunities.md) | GET | Retrieves a list of opportunities from Insightly. |
| [Search Opportunities](actions/search-opportunities.md) | GET | Finds opportunities in Insightly by search filters. |
| [Update Opportunity](actions/update-opportunity.md) | PUT | Updates an existing opportunity in Insightly. |

### Organisation

| Action | Method | Description |
| --- | --- | --- |
| [Create Organisation](actions/create-organisation.md) | POST | Creates a new organisation in Insightly. |
| [Get Organisation](actions/get-organisation.md) | GET | Retrieves an organisation from Insightly by ID. |
| [List Organisations](actions/list-organisations.md) | GET | Retrieves a list of organisations from Insightly. |
| [Search Organisations](actions/search-organisations.md) | GET | Finds organisations in Insightly by search filters. |
| [Update Organisation](actions/update-organisation.md) | PUT | Updates an existing organisation in Insightly. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Insightly. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Insightly by ID. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Insightly. |
| [Search Projects](actions/search-projects.md) | GET | Finds projects in Insightly by search filters. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Insightly. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Insightly. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Insightly by ID. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from Insightly. |
| [Search Tasks](actions/search-tasks.md) | GET | Finds tasks in Insightly by search filters. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Insightly. |

