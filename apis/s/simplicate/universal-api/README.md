# <img src="https://images.mindcloud.co/apps/icons/simplicate_1773948311133.png" alt="Simplicate logo" width="28" height="28"> Simplicate: Universal API

Manage CRM, projects, hours, invoices, and HR workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/simplicate/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.simplicate.com/
- **Vendor API docs:** https://developer.simplicate.com/docs/api/v2/getting_started/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Create Employee](actions/create-employee.md) | POST |  |
| [Get Employee](actions/get-employee.md) | GET |  |
| [List Employees](actions/list-employees.md) | GET |  |
| [Update Employee](actions/update-employee.md) | PUT |  |

### Hour Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Hour Entry](actions/create-hour-entry.md) | POST |  |
| [Get Hour Entry](actions/get-hour-entry.md) | GET |  |
| [List Hours](actions/list-hours.md) | GET |  |
| [Update Hour Entry](actions/update-hour-entry.md) | PUT |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |
| [Update Invoice](actions/update-invoice.md) | PUT |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST |  |
| [Get Organization](actions/get-organization.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |
| [Update Organization](actions/update-organization.md) | PUT |  |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST |  |
| [List Payments](actions/list-payments.md) | GET |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST |  |
| [Get Person](actions/get-person.md) | GET |  |
| [List Persons](actions/list-persons.md) | GET |  |
| [Update Person](actions/update-person.md) | PUT |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Project Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Service](actions/get-service.md) | GET |  |
| [List Services](actions/list-services.md) | GET |  |

### Quote Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote Template](actions/create-quote-template.md) | POST |  |
| [Get Quote Template](actions/get-quote-template.md) | GET |  |
| [List Quote Templates](actions/list-quote-templates.md) | GET |  |
| [Update Quote Template](actions/update-quote-template.md) | PUT |  |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [Create Sale](actions/create-sale.md) | POST |  |
| [Get Sale](actions/get-sale.md) | GET |  |
| [List Sales](actions/list-sales.md) | GET |  |
| [Update Sale](actions/update-sale.md) | PUT |  |

