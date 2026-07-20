# <img src="https://images.mindcloud.co/apps/icons/i-riskash-flow_1774022289243.png" alt="IRIS KashFlow logo" width="28" height="28"> IRIS KashFlow: Universal API

IRIS KashFlow is online accounting software for small businesses and accountants, covering quotes, invoicing, purchases, reporting, payments, and bookkeeping workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iRISKashFlow/latest
- **Category:** Commerce / Accounting
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.kashflow.com
- **Vendor API docs:** https://www.kashflow.com/developers/soap-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Details](actions/get-company-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iRISKashFlow/latest/actions/get-company-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Company Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Details](actions/get-company-details.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer by ID](actions/get-customer-by-id.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET |  |
| [List Customers Modified Since](actions/list-customers-modified-since.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice by ID](actions/get-invoice-by-id.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices for Customer](actions/list-invoices-for-customer.md) | GET |  |
| [List Recent Invoices](actions/list-recent-invoices.md) | GET |  |
| [List Unpaid Invoices](actions/list-unpaid-invoices.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET |  |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Quote by ID](actions/get-quote-by-id.md) | GET |  |

### Quotes

| Action | Method | Description |
| --- | --- | --- |
| [List Quotes for Customer](actions/list-quotes-for-customer.md) | GET |  |
| [List Recent Quotes](actions/list-recent-quotes.md) | GET |  |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Get Supplier by ID](actions/get-supplier-by-id.md) | GET |  |

### Suppliers

| Action | Method | Description |
| --- | --- | --- |
| [List Suppliers](actions/list-suppliers.md) | GET |  |

