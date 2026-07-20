# <img src="https://images.mindcloud.co/apps/icons/orderry_1774878767592.png" alt="Orderry logo" width="28" height="28"> Orderry: Universal API

Orderry is a field service and business operations platform for repair shops and service businesses. This app exposes Orderry's public API for contacts, orders, estimates, bookings, inventory, tasks, payments, and settings.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/orderry/latest
- **Actions:** 45
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://orderry.com
- **Vendor API docs:** https://orderry.readme.io/reference/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Settings](actions/get-company-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderry/latest/actions/get-company-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (45)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Settings](actions/get-company-settings.md) | GET |  |
| [Get Company Taxes](actions/get-company-taxes.md) | GET | Retrieves company tax rates from Orderry. |
| [Get Organization by ID](actions/get-organization-by-id.md) | GET | Retrieves an organization by ID from Orderry. |
| [Get Person by ID](actions/get-person-by-id.md) | GET | Retrieves a person by ID from Orderry. |
| [Get Product by ID](actions/get-product-by-id.md) | GET | Retrieves a product by ID from Orderry. |
| [Get Service by ID](actions/get-service-by-id.md) | GET | Retrieves a service by ID from Orderry. |
| [List Ad Campaigns](actions/list-ad-campaigns.md) | GET |  |
| [List Asset Custom Fields](actions/list-asset-custom-fields.md) | GET |  |
| [List Asset Directories](actions/list-asset-directories.md) | GET |  |
| [List Assets](actions/list-assets.md) | GET |  |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves a list of bookings from Orderry. |
| [List Cashbox Transactions](actions/list-cashbox-transactions.md) | GET |  |
| [List Cashboxes](actions/list-cashboxes.md) | GET |  |
| [List Employees](actions/list-employees.md) | GET | Retrieves a list of employees from Orderry. |
| [List Estimate Statuses](actions/list-estimate-statuses.md) | GET | Retrieves a list of estimate statuses from Orderry. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves a list of estimates from Orderry. |
| [List Inventory Postings](actions/list-inventory-postings.md) | GET |  |
| [List Inventory Transfers](actions/list-inventory-transfers.md) | GET |  |
| [List Inventory Write-Offs](actions/list-inventory-write-offs.md) | GET |  |
| [List Invoice Statuses](actions/list-invoice-statuses.md) | GET | Retrieves a list of invoice statuses from Orderry. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves a list of invoices from Orderry. |
| [List Lead Custom Fields](actions/list-lead-custom-fields.md) | GET |  |
| [List Lead Statuses](actions/list-lead-statuses.md) | GET |  |
| [List Lead Types](actions/list-lead-types.md) | GET |  |
| [List Leads](actions/list-leads.md) | GET |  |
| [List Location Resources](actions/list-location-resources.md) | GET | Retrieves a list of location resources from Orderry. |
| [List Locations](actions/list-locations.md) | GET | Retrieves a list of company locations from Orderry. |
| [List Order Custom Fields](actions/list-order-custom-fields.md) | GET | Retrieves a list of order custom fields from Orderry. |
| [List Order Statuses](actions/list-order-statuses.md) | GET | Retrieves a list of order statuses from Orderry. |
| [List Order Types](actions/list-order-types.md) | GET | Retrieves a list of order types from Orderry. |
| [List Orders](actions/list-orders.md) | GET | Retrieves a list of orders from Orderry. |
| [List Organization People](actions/list-organization-people.md) | GET | Retrieves people for an organization from Orderry. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves a list of organizations from Orderry. |
| [List People](actions/list-people.md) | GET | Retrieves a list of people from Orderry. |
| [List Person Organizations](actions/list-person-organizations.md) | GET | Retrieves a person's organization from Orderry. |
| [List Prices](actions/list-prices.md) | GET |  |
| [List Product Categories](actions/list-product-categories.md) | GET | Retrieves a list of product categories from Orderry. |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from Orderry. |
| [List Sales](actions/list-sales.md) | GET | Retrieves a list of sales from Orderry. |
| [List Service Categories](actions/list-service-categories.md) | GET | Retrieves a list of service categories from Orderry. |
| [List Services](actions/list-services.md) | GET | Retrieves a list of services from Orderry. |
| [List Stock](actions/list-stock.md) | GET |  |
| [List Units of Measurement](actions/list-units-of-measurement.md) | GET |  |
| [List Warehouse Bins](actions/list-warehouse-bins.md) | GET |  |
| [List Warehouses](actions/list-warehouses.md) | GET |  |

