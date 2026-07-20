# <img src="https://images.mindcloud.co/apps/icons/zahara_1774544291926.png" alt="Zahara logo" width="28" height="28"> Zahara: Universal API

Manage Zahara invoices, purchase orders, suppliers, projects, users, and tenancy data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zahara/latest
- **Category:** Commerce / Procurement
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zaharasoftware.com
- **Vendor API docs:** https://ask.zaharasoftware.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users (Business Unit)](actions/list-users-business-unit.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-users-business-unit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Business Unit

| Action | Method | Description |
| --- | --- | --- |
| [List Business Units](actions/list-business-units.md) | GET | Retrieves business units from a Zahara tenancy. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves available currencies from the Zahara tenancy. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Zahara. |
| [Get Invoice By ID](actions/get-invoice-by-id.md) | GET | Retrieves an invoice by ID from Zahara. |
| [List Invoices After Date](actions/list-invoices-after-date.md) | GET | Retrieves invoices from Zahara after a specific date. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Zahara. |
| [Upload Invoice PDF](actions/upload-invoice-pdf.md) | PUT | Updates an invoice in Zahara by uploading its PDF. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Zahara. |
| [Get Project By ID](actions/get-project-by-id.md) | GET | Retrieves a project by ID from Zahara. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from a Zahara business unit. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Zahara. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order](actions/create-purchase-order.md) | POST | Creates a new purchase order in Zahara. |
| [Get Purchase Order By ID](actions/get-purchase-order-by-id.md) | GET | Retrieves a purchase order by ID from Zahara. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from a Zahara business unit. |
| [List Purchase Orders After Date](actions/list-purchase-orders-after-date.md) | GET | Retrieves purchase orders from Zahara after a specific date. |
| [Update Purchase Order](actions/update-purchase-order.md) | PUT | Updates an existing purchase order in Zahara. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier](actions/create-supplier.md) | POST | Creates a new supplier in Zahara. |
| [Get Supplier By ID](actions/get-supplier-by-id.md) | GET | Retrieves a supplier by ID from Zahara. |
| [List Suppliers After Date](actions/list-suppliers-after-date.md) | GET | Retrieves suppliers from Zahara after a specific date. |
| [Search Suppliers](actions/search-suppliers.md) | GET | Finds suppliers in Zahara by search term. |
| [Update Supplier](actions/update-supplier.md) | PUT | Updates an existing supplier in Zahara. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users (Business Unit)](actions/list-users-business-unit.md) | GET | Retrieves users from a Zahara business unit. |
| [List Users (Tenancy)](actions/list-users-tenancy.md) | GET | Retrieves users from a Zahara tenancy. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from a Zahara business unit. |

