# <img src="https://images.mindcloud.co/apps/icons/idl-bs-yi-yy9-logos_1773947287113.jpeg" alt="Simpro logo" width="28" height="28"> Simpro: Universal API

Manage jobs, customers, quotes, and invoices in Simpro

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/simpro/latest
- **Category:** Support / Field Service
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.simprogroup.com/
- **Vendor API docs:** https://developer.simprogroup.com/apidoc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Companies](actions/list-companies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Catalog

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Item](actions/get-catalog-item.md) | GET |  |
| [List Catalogs](actions/list-catalogs.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Get Customer](actions/get-customer.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |

### Customer Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Payments](actions/list-customer-payments.md) | GET |  |

### Inventory Item

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Items](actions/list-inventory-items.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST |  |
| [Get Job](actions/get-job.md) | GET |  |
| [List Jobs](actions/list-jobs.md) | GET |  |
| [Update Job](actions/update-job.md) | PUT |  |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote](actions/create-quote.md) | POST |  |
| [Get Quote](actions/get-quote.md) | GET |  |
| [List Quotes](actions/list-quotes.md) | GET |  |
| [Update Quote](actions/update-quote.md) | PUT |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Schedules](actions/list-schedules.md) | GET |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST |  |
| [Get Site](actions/get-site.md) | GET |  |
| [List Sites](actions/list-sites.md) | GET |  |
| [Update Site](actions/update-site.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### Work Order

| Action | Method | Description |
| --- | --- | --- |
| [List Work Orders / Job Cards](actions/list-work-orders-job-cards.md) | GET |  |

