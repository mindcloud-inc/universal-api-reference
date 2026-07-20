# <img src="https://images.mindcloud.co/apps/icons/conta-azul-icon-square_1775767753815.png" alt="Conta Azul logo" width="28" height="28"> Conta Azul: Universal API

Conta Azul Pro ERP API for people, inventory, sales, finance, contracts, acquittances, and invoices using OAuth 2.0 bearer tokens.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/contaAzulAPI/latest
- **Category:** Commerce / Accounting
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://contaazul.com
- **Vendor API docs:** https://developers.contaazul.com/auth

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Connected Company](actions/get-connected-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-connected-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Financial Account Current Balance](actions/get-financial-account-current-balance.md) | GET |  |
| [List Financial Accounts](actions/list-financial-accounts.md) | GET |  |

### Bills

| Action | Method | Description |
| --- | --- | --- |
| [Search Accounts Payable](actions/search-accounts-payable.md) | GET |  |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET |  |
| [List DRE Categories](actions/list-dre-categories.md) | GET |  |
| [List Ecommerce Categories](actions/list-ecommerce-categories.md) | GET |  |
| [List Product Categories](actions/list-product-categories.md) | GET |  |
| [List Product CESTs](actions/list-product-cests.md) | GET |  |
| [List Product NCMs](actions/list-product-ncms.md) | GET |  |

### Company Infos

| Action | Method | Description |
| --- | --- | --- |
| [Get Connected Company](actions/get-connected-company.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Person](actions/get-person.md) | GET |  |
| [Get Person By Legacy ID](actions/get-person-by-legacy-id.md) | GET |  |
| [List People](actions/list-people.md) | GET |  |

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [Get Next Contract Number](actions/get-next-contract-number.md) | GET |  |
| [List Contracts](actions/list-contracts.md) | GET |  |

### Cost Centers

| Action | Method | Description |
| --- | --- | --- |
| [List Cost Centers](actions/list-cost-centers.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Sale Printable](actions/get-sale-printable.md) | GET |  |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [List Salespeople](actions/list-salespeople.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice By Key](actions/get-invoice-by-key.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |
| [List Service Invoices](actions/list-service-invoices.md) | GET |  |
| [Search Accounts Receivable](actions/search-accounts-receivable.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Financial Installment](actions/get-financial-installment.md) | GET |  |
| [List Changed Financial Events](actions/list-changed-financial-events.md) | GET |  |
| [List Financial Event Installments](actions/list-financial-event-installments.md) | GET |  |
| [List Financial Transfers](actions/list-financial-transfers.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET |  |
| [List Ecommerce Brands](actions/list-ecommerce-brands.md) | GET |  |
| [List Product Units Of Measure](actions/list-product-units-of-measure.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [List Opening Balances](actions/list-opening-balances.md) | GET |  |

### Sales Order Lines

| Action | Method | Description |
| --- | --- | --- |
| [List Sale Items](actions/list-sale-items.md) | GET |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Next Sale Number](actions/get-next-sale-number.md) | GET |  |
| [Get Sale](actions/get-sale.md) | GET |  |
| [Search Sales](actions/search-sales.md) | GET |  |

### Settlements

| Action | Method | Description |
| --- | --- | --- |
| [Get Acquittance](actions/get-acquittance.md) | GET |  |
| [List Acquittances By Installment](actions/list-acquittances-by-installment.md) | GET |  |

