# <img src="https://images.mindcloud.co/apps/icons/synergy-crm_1776713064528.png" alt="SynergyCRM logo" width="28" height="28"> SynergyCRM: Universal API

Connect SynergyCRM with MindCloud to read CRM contacts, companies, deals, orders, products, tasks, entries, projects, and related status/reference records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/synergyCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://synergycrm.ru/
- **Vendor API docs:** https://api.synergycrm.ru/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synergyCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Entry](actions/get-entry.md) | GET |  |
| [List Entries](actions/list-entries.md) | GET |  |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Deal Stage Category](actions/get-deal-stage-category.md) | GET |  |
| [Get Product Category](actions/get-product-category.md) | GET |  |
| [Get Product Type](actions/get-product-type.md) | GET |  |
| [List Deal Stage Categories](actions/list-deal-stage-categories.md) | GET |  |
| [List Product Categories](actions/list-product-categories.md) | GET |  |
| [List Product Types](actions/list-product-types.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Get Deal](actions/get-deal.md) | GET |  |
| [List Deals](actions/list-deals.md) | GET |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Stages

| Action | Method | Description |
| --- | --- | --- |
| [Get Deal Stage](actions/get-deal-stage.md) | GET |  |
| [List Deal Stages](actions/list-deal-stages.md) | GET |  |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Deal Status](actions/get-deal-status.md) | GET |  |
| [Get Order Status](actions/get-order-status.md) | GET |  |
| [Get Product Status](actions/get-product-status.md) | GET |  |
| [List Deal Statuses](actions/list-deal-statuses.md) | GET |  |
| [List Order Statuses](actions/list-order-statuses.md) | GET |  |
| [List Product Statuses](actions/list-product-statuses.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Diary Task](actions/get-diary-task.md) | GET |  |
| [List Diary Tasks](actions/list-diary-tasks.md) | GET |  |

