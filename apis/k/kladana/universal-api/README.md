# <img src="https://images.mindcloud.co/apps/icons/kladana_1776786633518.png" alt="Kladana logo" width="28" height="28"> Kladana: Universal API

Kladana is a cloud ERP platform for inventory, sales, purchases, warehouses, manufacturing, CRM records, and operational reporting.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kladana/latest
- **Category:** Commerce
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.kladana.com/
- **Vendor API docs:** https://dev.kladana.com/doc/api/remap/1.2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Employee Context](actions/get-current-employee-context.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-current-employee-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Assortment

| Action | Method | Description |
| --- | --- | --- |
| [List Assortment](actions/list-assortment.md) | GET | Lists assortment items in your Kladana account. |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [List Batches](actions/list-batches.md) | GET | Lists batches in your Kladana account. |

### Brief Stock Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Brief Stock Report](actions/get-brief-stock-report.md) | GET | Retrieves the brief stock report from Kladana. |

### Bundle

| Action | Method | Description |
| --- | --- | --- |
| [List Bundles](actions/list-bundles.md) | GET | Lists bundles in your Kladana account. |

### Company Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Settings](actions/get-company-settings.md) | GET | Retrieves company settings details from Kladana. |

### Contract

| Action | Method | Description |
| --- | --- | --- |
| [List Contracts](actions/list-contracts.md) | GET | Lists contracts in your Kladana account. |

### Counterparty

| Action | Method | Description |
| --- | --- | --- |
| [Get Counterparty](actions/get-counterparty.md) | GET | Retrieves a counterparty record from Kladana. |
| [List Counterparties](actions/list-counterparties.md) | GET | Lists counterparties in your Kladana account. |

### Counterparty Indicators

| Action | Method | Description |
| --- | --- | --- |
| [Get Counterparty Indicators](actions/get-counterparty-indicators.md) | GET | Retrieves counterparty indicators report from Kladana. |

### Counterparty Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Counterparty Metadata](actions/get-counterparty-metadata.md) | GET | Retrieves counterparty metadata details from Kladana. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Lists countries in your Kladana account. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Lists currencies in your Kladana account. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Employee Context](actions/get-current-employee-context.md) | GET | Retrieves current employee context from Kladana. |
| [List Employees](actions/list-employees.md) | GET | Lists employees in your Kladana account. |

### Incoming Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Incoming Payments](actions/list-incoming-payments.md) | GET | Lists incoming payments in your Kladana account. |

### Inventory Count

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Counts](actions/list-inventory-counts.md) | GET | Lists inventory counts in your Kladana account. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Lists organizations in your Kladana account. |

### Outgoing Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Outgoing Payments](actions/list-outgoing-payments.md) | GET | Lists outgoing payments in your Kladana account. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product record from Kladana. |
| [List Products](actions/list-products.md) | GET | Lists products in your Kladana account. |

### Product Directory Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Directory Settings](actions/get-product-directory-settings.md) | GET | Retrieves product directory settings from Kladana. |

### Product Group

| Action | Method | Description |
| --- | --- | --- |
| [List Product Groups](actions/list-product-groups.md) | GET | Lists product groups in your Kladana account. |

### Product Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Metadata](actions/get-product-metadata.md) | GET | Retrieves product metadata details from Kladana. |

### Product Variant

| Action | Method | Description |
| --- | --- | --- |
| [List Product Variants](actions/list-product-variants.md) | GET | Lists product variants in your Kladana account. |

### Product Variant Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Variant Metadata](actions/get-product-variant-metadata.md) | GET | Retrieves product variant metadata from Kladana. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Lists projects in your Kladana account. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Lists purchase orders in your Kladana account. |

### Receiving

| Action | Method | Description |
| --- | --- | --- |
| [List Receivings](actions/list-receivings.md) | GET | Lists receivings in your Kladana account. |

### Sales Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Invoices](actions/list-sales-invoices.md) | GET | Lists sales invoices in your Kladana account. |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Sales Order](actions/get-sales-order.md) | GET | Retrieves a sales order from Kladana. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Lists sales orders in your Kladana account. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Service](actions/get-service.md) | GET | Retrieves a service record from Kladana. |
| [List Services](actions/list-services.md) | GET | Lists services in your Kladana account. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment record from Kladana. |
| [List Shipments](actions/list-shipments.md) | GET | Lists shipments in your Kladana account. |

### Stock Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Advanced Stock Report](actions/get-advanced-stock-report.md) | GET | Retrieves the advanced stock report from Kladana. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Subscription](actions/get-company-subscription.md) | GET | Retrieves company subscription details from Kladana. |

### Supplier Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Supplier Invoices](actions/list-supplier-invoices.md) | GET | Lists supplier invoices in your Kladana account. |

### Unit Of Measure

| Action | Method | Description |
| --- | --- | --- |
| [List Units Of Measure](actions/list-units-of-measure.md) | GET | Lists units of measure in Kladana. |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [List Warehouses](actions/list-warehouses.md) | GET | Lists warehouses in your Kladana account. |

