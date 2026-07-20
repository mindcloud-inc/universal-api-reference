# <img src="https://images.mindcloud.co/apps/icons/images-5_1774644999659.png" alt="Priority logo" width="28" height="28"> Priority: Universal API

ERP platform with a REST/OData API for business objects, forms, and operational workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/priority/latest
- **Category:** Commerce / ERP
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.priority-software.com/
- **Vendor API docs:** https://prioritysoftware.github.io/restapi/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Priority Version](actions/get-priority-version.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-priority-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Ap Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get AP Invoice](actions/get-ap-invoice.md) | GET | Retrieves an AP invoice from Priority. |
| [List AP Invoices](actions/list-ap-invoices.md) | GET | Retrieves AP invoices from Priority. |

### Ar Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get AR Invoice](actions/get-ar-invoice.md) | GET | Retrieves an AR invoice from Priority. |
| [List AR Invoices](actions/list-ar-invoices.md) | GET | Retrieves AR invoices from Priority. |

### Bank

| Action | Method | Description |
| --- | --- | --- |
| [Get Bank](actions/get-bank.md) | GET | Retrieves a bank from Priority. |
| [List Banks](actions/list-banks.md) | GET | Retrieves banks from Priority. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Priority. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Priority. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [Get Country](actions/get-country.md) | GET | Retrieves a country from Priority. |
| [List Countries](actions/list-countries.md) | GET | Retrieves countries from Priority. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [Get Currency](actions/get-currency.md) | GET | Retrieves a currency from Priority. |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves currencies from Priority. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Priority. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Priority. |

### Customer Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Document](actions/get-customer-document.md) | GET | Retrieves a customer document from Priority. |
| [List Customer Documents](actions/list-customer-documents.md) | GET | Retrieves customer documents from Priority. |

### Document Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Type](actions/get-document-type.md) | GET | Retrieves a document type from Priority. |
| [List Document Types](actions/list-document-types.md) | GET | Retrieves document types from Priority. |

### Part

| Action | Method | Description |
| --- | --- | --- |
| [Get Part](actions/get-part.md) | GET | Retrieves a part from Priority. |
| [List Parts](actions/list-parts.md) | GET | Retrieves parts from Priority. |

### Part Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Part Balance](actions/get-part-balance.md) | GET | Retrieves a part balance from Priority. |
| [List Part Balances](actions/list-part-balances.md) | GET | Retrieves part balances from Priority. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase Order](actions/get-purchase-order.md) | GET | Retrieves a purchase order from Priority. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from Priority. |

### Quotation Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Quotation Document](actions/get-quotation-document.md) | GET | Retrieves a quotation document from Priority. |
| [List Quotation Documents](actions/list-quotation-documents.md) | GET | Retrieves quotation documents from Priority. |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Sales Order](actions/get-sales-order.md) | GET | Retrieves a sales order from Priority. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves sales orders from Priority. |

### Shipper

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipper](actions/get-shipper.md) | GET | Retrieves a shipper from Priority. |
| [List Shippers](actions/list-shippers.md) | GET | Retrieves shippers from Priority. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get OData Version](actions/get-o-data-version.md) | GET | Retrieves the OData version from Priority. |
| [Get Priority Version](actions/get-priority-version.md) | GET | Retrieves the Priority version. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Get Supplier](actions/get-supplier.md) | GET | Retrieves a supplier from Priority. |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from Priority. |

### Tenant

| Action | Method | Description |
| --- | --- | --- |
| [Get Tenant Details](actions/get-tenant-details.md) | GET | Retrieves tenant details from Priority. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Login Name](actions/get-login-name.md) | GET | Retrieves the current login name from Priority. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Priority. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Priority. |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [Get Warehouse](actions/get-warehouse.md) | GET | Retrieves a warehouse from Priority. |
| [List Warehouses](actions/list-warehouses.md) | GET | Retrieves warehouses from Priority. |

