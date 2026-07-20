# IRIS KashFlow: Native API Reference

A consolidated summary of IRIS KashFlow's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://www.kashflow.com/developers/soap-api/
- **API base URL:** `https://securedwebapp.com`

## Authentication

### SOAP Username + Password

Authenticate KashFlow SOAP requests with the account username and the web password or separate API password configured in KashFlow API Settings.

### Credentials

- **Username:** `username` · required · Your KashFlow account username.
- **Password:** `password` · required · Use your normal KashFlow password or the separate API password, depending on the API Settings configuration.

[Official authentication documentation](https://www.kashflow.com/support/kb/enabling-the-api/)

## API conventions

Responses from this API use XML. Response data is read from `Result`.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Company Details](actions/get-company-details.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getcompanydetails/) |
| [Get Customer by ID](actions/get-customer-by-id.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getcustomerbyid/) |
| [Get Invoice by ID](actions/get-invoice-by-id.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getinvoicebyid/) |
| [Get Quote by ID](actions/get-quote-by-id.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getquotebyid/) |
| [Get Supplier by ID](actions/get-supplier-by-id.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getsupplierbyid/) |
| [List Customers](actions/list-customers.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getcustomers/) |
| [List Customers Modified Since](actions/list-customers-modified-since.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getcustomersmodifiedsince/) |
| [List Invoices for Customer](actions/list-invoices-for-customer.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getinvoicesforcustomer/) |
| [List Products](actions/list-products.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getproducts/) |
| [List Quotes for Customer](actions/list-quotes-for-customer.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getquotesforcustomer/) |
| [List Recent Invoices](actions/list-recent-invoices.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getinvoices-recent/) |
| [List Recent Quotes](actions/list-recent-quotes.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getquotes-recent/) |
| [List Suppliers](actions/list-suppliers.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getsuppliers/) |
| [List Unpaid Invoices](actions/list-unpaid-invoices.md) | `POST /api/service.asmx` | [docs](https://www.kashflow.com/developers/soap-api/getinvoices-unpaid/) |
