# <img src="https://images.mindcloud.co/apps/icons/365_1776859891830.png" alt="Microsoft Dynamics 365 BC logo" width="28" height="28"> Microsoft Dynamics 365 BC: Universal API

Microsoft Dynamics 365 Business Central

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoftDynamics365BC/latest
- **Actions:** 52
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Create Credit Memo Itens ODataV4](actions/create-credit-memo-itens-o-data-v4.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-credit-memo-itens-o-data-v4?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (52)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Create Ship-to Addresses SSI](actions/create-ship-to-addresses-ssi.md) | POST |  |
| [Get Inventory By Location SSI](actions/get-inventory-by-location-ssi.md) | GET |  |
| [Get Ship-to Addresses SSI](actions/get-ship-to-addresses-ssi.md) | GET |  |
| [Update Ship-to Addresses SSI](actions/update-ship-to-addresses-ssi.md) | PUT |  |

### Company Infos

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Costumer ODataV4](actions/create-costumer-o-data-v4.md) | POST |  |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Create Customer SSI](actions/create-customer-ssi.md) | POST |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [List Customers ODataV4](actions/list-customers-o-data-v4.md) | GET |  |
| [List Customers SSI](actions/list-customers-ssi.md) | GET |  |
| [List Employees ODataV4](actions/list-employees-o-data-v4.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Post Journal Lines](actions/post-journal-lines.md) | PUT |  |
| [Update Costumer ODataV4](actions/update-costumer-o-data-v4.md) | PUT |  |
| [Update Costumer SSI](actions/update-costumer-ssi.md) | PUT |  |
| [Update Dimension](actions/update-dimension.md) | PUT |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Credit Memo](actions/create-credit-memo.md) | POST |  |
| [Create Credit Memo Line Item](actions/create-credit-memo-line-item.md) | POST |  |
| [Create Sales Invoice Line Item](actions/create-sales-invoice-line-item.md) | POST |  |
| [Create Sales Invoices](actions/create-sales-invoices.md) | POST |  |
| [Delete Sales Invoice Line Item](actions/delete-sales-invoice-line-item.md) | DELETE |  |
| [List Sales Invoice](actions/list-sales-invoice.md) | GET |  |
| [List Sales Invoice Line Items](actions/list-sales-invoice-line-items.md) | GET |  |
| [Post Credit Memo](actions/post-credit-memo.md) | POST |  |
| [Post Sales Invoice](actions/post-sales-invoice.md) | POST |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Job Planning Lines ODataV4](actions/create-project-job-planning-lines-o-data-v4.md) | POST |  |
| [Create Project Job Task Lines ODataV4](actions/create-project-job-task-lines-o-data-v4.md) | POST |  |
| [List Items](actions/list-items.md) | GET |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Bank Deposit Lines ODataV4](actions/create-bank-deposit-lines-o-data-v4.md) | POST |  |
| [Create Bank Deposit ODataV4](actions/create-bank-deposit-o-data-v4.md) | POST |  |
| [Create Credit Memo Itens ODataV4](actions/create-credit-memo-itens-o-data-v4.md) | GET |  |
| [Create General Journal ODataV4](actions/create-general-journal-o-data-v4.md) | POST |  |
| [Create Journal Line ODataV4](actions/create-journal-line-o-data-v4.md) | POST |  |
| [List Bank Deposits Line ODataV4](actions/list-bank-deposits-line-o-data-v4.md) | GET |  |
| [List Bank Deposits ODataV4](actions/list-bank-deposits-o-data-v4.md) | GET |  |
| [List Credit Memo ODataV4](actions/list-credit-memo-o-data-v4.md) | GET |  |
| [List Customer Ledger Entries ODataV4](actions/list-customer-ledger-entries-o-data-v4.md) | GET |  |
| [List General Journal ODataV4](actions/list-general-journal-o-data-v4.md) | GET |  |
| [List Journal Lines Payments ODataV4](actions/list-journal-lines-payments-o-data-v4.md) | GET |  |
| [List Payroll Journal ODataV4](actions/list-payroll-journal-o-data-v4.md) | GET |  |
| [List Sales Invoice ODataV4](actions/list-sales-invoice-o-data-v4.md) | GET |  |
| [Update Customer Payment ODataV4](actions/update-customer-payment-o-data-v4.md) | POST |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Order](actions/create-sales-order.md) | POST |  |
| [Create Sales Order SSI](actions/create-sales-order-ssi.md) | POST |  |
| [Create Sales Order Line](actions/create-sales-orders-lines.md) | POST |  |
| [List Journal Line](actions/list-journal-line.md) | GET |  |
| [List Sales Orders Lines SSI](actions/list-sales-orders-lines-ssi.md) | GET |  |
| [List Sales Orders SSI](actions/list-sales-orders-ssi.md) | GET |  |
| [Update Sales Order SSI](actions/update-sales-order-ssi.md) | POST |  |
| [Update Sales Orders Lines](actions/update-sales-orders-lines.md) | PUT |  |

