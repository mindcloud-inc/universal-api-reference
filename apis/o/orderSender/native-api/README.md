# Order Sender: Native API Reference

A consolidated summary of Order Sender's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://developer.ordersender.com/
- **OpenAPI specification:** https://developer.ordersender.com/api/API.json?v=1.4.2
- **API base URL:** `https://business.ordersender.com/api/v1`

## Authentication

### Order Sender Credentials

Order Sender Business requires the company code and OSBusiness API token on every request.

### Credentials

- **Company Code:** `cod` · required · Order Sender company code required on every API request.
- **API Token:** `token` · required · OSBusiness API token generated in API Management and required on every request.

[Official authentication documentation](https://developer.ordersender.com/)

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Customers](actions/delete-customers.md) | `POST /op/delete/res/clienti` | [docs](https://developer.ordersender.com/) |
| [Delete Discounts](actions/delete-discounts.md) | `POST /op/delete/res/sconti` | [docs](https://developer.ordersender.com/) |
| [Delete Payment Conditions](actions/delete-payment-conditions.md) | `POST /op/delete/res/condizioni_pagamento` | [docs](https://developer.ordersender.com/) |
| [Delete Products](actions/delete-products.md) | `POST /op/delete/res/prodotti` | [docs](https://developer.ordersender.com/) |
| [Delete Prospects](actions/delete-prospects.md) | `POST /op/delete/res/prospect` | [docs](https://developer.ordersender.com/) |
| [Delete Secondary Addresses](actions/delete-secondary-addresses.md) | `POST /op/delete/res/sedi` | [docs](https://developer.ordersender.com/) |
| [Import Commissions](actions/import-commissions.md) | `POST /op/import/res/provvigioni` | [docs](https://developer.ordersender.com/) |
| [Import Customer Payment Conditions](actions/import-customer-payment-conditions.md) | `POST /op/import/res/clienti_pagamenti` | [docs](https://developer.ordersender.com/) |
| [Import Customers](actions/import-customers.md) | `POST /op/import/res/clienti` | [docs](https://developer.ordersender.com/) |
| [Import Discounts](actions/import-discounts.md) | `POST /op/import/res/sconti` | [docs](https://developer.ordersender.com/) |
| [Import Payment Conditions](actions/import-payment-conditions.md) | `POST /op/import/res/condizioni_pagamento` | [docs](https://developer.ordersender.com/) |
| [Import Price Lists](actions/import-price-lists.md) | `POST /op/import/res/listini` | [docs](https://developer.ordersender.com/) |
| [Import Products](actions/import-products.md) | `POST /op/import/res/prodotti` | [docs](https://developer.ordersender.com/) |
| [Import Prospects](actions/import-prospects.md) | `POST /op/import/res/prospect` | [docs](https://developer.ordersender.com/) |
| [Import Secondary Addresses](actions/import-secondary-addresses.md) | `POST /op/import/res/sedi` | [docs](https://developer.ordersender.com/) |
| [Import Suppliers](actions/import-suppliers.md) | `POST /op/import/res/fornitori` | [docs](https://developer.ordersender.com/) |
| [List Commissions](actions/list-commissions.md) | `GET /op/export/res/provvigioni` | [docs](https://developer.ordersender.com/) |
| [List Customer Payment Conditions](actions/list-customer-payment-conditions.md) | `GET /op/export/res/clienti_pagamenti` | [docs](https://developer.ordersender.com/) |
| [List Customers](actions/list-customers.md) | `GET /op/export/res/clienti` | [docs](https://developer.ordersender.com/) |
| [List Discounts](actions/list-discounts.md) | `GET /op/export/res/sconti` | [docs](https://developer.ordersender.com/) |
| [List Orders](actions/list-orders.md) | `GET /op/export/res/ordini` | [docs](https://developer.ordersender.com/) |
| [List Payment Conditions](actions/list-payment-conditions.md) | `GET /op/export/res/condizioni_pagamento` | [docs](https://developer.ordersender.com/) |
| [List Price Lists](actions/list-price-lists.md) | `GET /op/export/res/listini` | [docs](https://developer.ordersender.com/) |
| [List Products](actions/list-products.md) | `GET /op/export/res/prodotti` | [docs](https://developer.ordersender.com/) |
| [List Prospects](actions/list-prospects.md) | `GET /op/export/res/prospect` | [docs](https://developer.ordersender.com/) |
| [List Quotes](actions/list-quotes.md) | `GET /op/export/res/preventivi` | [docs](https://developer.ordersender.com/) |
| [List Suppliers](actions/list-suppliers.md) | `GET /op/export/res/fornitori` | [docs](https://developer.ordersender.com/) |
| [Verify Connection](actions/verify-connection.md) | `GET /op/check` | [docs](https://developer.ordersender.com/) |
