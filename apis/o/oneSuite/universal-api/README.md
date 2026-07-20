# <img src="https://images.mindcloud.co/apps/icons/one-suite_1776701800248.png" alt="OneSuite logo" width="28" height="28"> OneSuite: Universal API

All-in-one business platform for agencies to manage CRM, projects, clients, invoices, and documents.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oneSuite/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://onesuite.io/
- **Vendor API docs:** https://rest-api.onesuite.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Opportunity Stages](actions/get-opportunity-stages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-opportunity-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Convert Company to Client](actions/convert-company-to-client.md) | PUT | Converts a company to a client in OneSuite. |
| [Create Company](actions/create-company.md) | POST | Creates a company in OneSuite. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from OneSuite. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from OneSuite. |
| [Update Company](actions/update-company.md) | PUT | Updates a company in OneSuite. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Connect Person to Company](actions/connect-person-to-company.md) | PUT | Connects a person to a company in OneSuite. |
| [Connect Person to Opportunity](actions/connect-person-to-opportunity.md) | PUT | Connects a person to an opportunity in OneSuite. |
| [Create Person](actions/create-person.md) | POST | Creates a person in OneSuite. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from OneSuite. |
| [List Company People](actions/list-company-people.md) | GET | Retrieves a company's people from OneSuite. |
| [List People](actions/list-people.md) | GET | Retrieves people from OneSuite. |
| [Update Person](actions/update-person.md) | PUT | Updates a person in OneSuite. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a client in OneSuite. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from OneSuite. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from OneSuite. |
| [Update Client](actions/update-client.md) | PUT | Updates a client in OneSuite. |
| [Update Client Priority](actions/update-client-priority.md) | PUT | Updates a client's priority in OneSuite. |
| [Update Client Status](actions/update-client-status.md) | PUT | Updates a client's status in OneSuite. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates an invoice in OneSuite. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from OneSuite. |
| [List Client Invoices](actions/list-client-invoices.md) | GET | Retrieves a client's invoices from OneSuite. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from OneSuite. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an invoice in OneSuite. |
| [Update Invoice Status](actions/update-invoice-status.md) | PUT | Updates an invoice payment status in OneSuite. |

### Opportunities

| Action | Method | Description |
| --- | --- | --- |
| [Connect Opportunity to Company](actions/connect-opportunity-to-company.md) | PUT | Connects an opportunity to a company in OneSuite. |
| [Convert Opportunity to Client](actions/convert-opportunity-to-client.md) | PUT | Converts an opportunity to a client in OneSuite. |
| [Create Opportunity](actions/create-opportunity.md) | POST | Creates an opportunity in OneSuite. |
| [Get Opportunity](actions/get-opportunity.md) | GET | Retrieves an opportunity from OneSuite. |
| [List Opportunities](actions/list-opportunities.md) | GET | Retrieves opportunities from OneSuite. |
| [Update Opportunity](actions/update-opportunity.md) | PUT | Updates an opportunity in OneSuite. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Client Project](actions/create-client-project.md) | POST | Creates a project for a client in OneSuite. |
| [Create Project](actions/create-project.md) | POST | Creates a project in OneSuite. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from OneSuite. |
| [List Client Projects](actions/list-client-projects.md) | GET | Retrieves a client's projects from OneSuite. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from OneSuite. |
| [Update Project](actions/update-project.md) | PUT | Updates a project in OneSuite. |

### Stages

| Action | Method | Description |
| --- | --- | --- |
| [Get Opportunity Stages](actions/get-opportunity-stages.md) | GET | Retrieves opportunity stages from OneSuite. |
| [Update Opportunity Stage](actions/update-opportunity-stage.md) | PUT | Updates an opportunity stage in OneSuite. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [List Section Tasks](actions/list-section-tasks.md) | GET | Retrieves tasks for a project section in OneSuite. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Project Sections](actions/list-project-sections.md) | GET | Retrieves sections for a project in OneSuite. |

