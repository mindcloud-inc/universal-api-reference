# BigCommerce (B2B): Native API Reference

A consolidated summary of BigCommerce (B2B)'s API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://developer.bigcommerce.com/b2b-edition/apis
- **API base URL:** `https://api-b2b.bigcommerce.com/api/v3/io/`

## Authentication

### Custom

### Credentials

- **Auth Token:** `authToken` · optional

Send these headers with each API request:

```http
authToken: <authToken>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Response data is read from `data`.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | `POST ip/invoices` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/invoice-management/invoice#create-invoice) |
| [Get All Companies](actions/get-all-companies.md) | `GET companies` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/company/companies) |
| [Get Company](actions/get-company.md) | `GET companies/:companyId` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/company/companies) |
| [Get Company Credit](actions/get-company-credit.md) | `GET companies/:companyId/credit` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/payment#get-company-credit) |
| [Get Company Payment Methods](actions/get-company-payment-methods.md) | `GET companies/:companyId/payments` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/payment#update-company-credit) |
| [Get Company Payment Terms](actions/get-company-payment-terms.md) | `GET companies/:companyId/payment-terms` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/payment#update-company-credit) |
| [Get Invoice](actions/get-invoice.md) | `GET ip/invoices/:invoiceid` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/invoice-management/invoice#get-invoice-detail) |
| [Get invoices](actions/get-invoices.md) | `GET ip/invoices` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/invoice-management/invoice#get-invoice-detail) |
| [Get Order](actions/get-order.md) | `GET https://api-b2b.bigcommerce.com/api/v3/io/orders/:orderId` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/invoice-management/invoice#get-invoice-detail) |
| [Update Company](actions/update-company.md) | `PUT companies/:companyId` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/payment#update-company-credit) |
| [Update Company Credit](actions/update-company-credit.md) | `PUT companies/:companyId/credit` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/payment#update-company-credit) |
| [Update Company Payment Methods](actions/update-company-payment-methods.md) | `PUT companies/:companyId/payments` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/payment#update-company-credit) |
| [Update Company Payment Terms](actions/update-company-payment-terms.md) | `PUT companies/:companyId/payment-terms` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/payment#update-company-credit) |
| [Update Invoice](actions/update-invoice.md) | `PUT ip/invoices/:invoiceId` | [docs](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/invoice-management/invoice#create-invoice) |
