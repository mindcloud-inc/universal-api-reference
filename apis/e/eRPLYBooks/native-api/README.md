# ERPLY Books: Native API Reference

A consolidated summary of ERPLY Books's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://learn-api.erply.com/requests
- **API base URL:** `https://{customerCode}.erply.com/api`

## Authentication

### Session Authentication

Authenticate with ERPLY using your account number, login email, and password to retrieve a reusable session key.

### Credentials

- **Customer Code:** `customerCode` · required
- **Username:** `username` · required
- **Password:** `password` · required

[Official authentication documentation](https://wiki.erply.com/en/article/1720)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Response data is read from `records`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST /` | [docs](https://wiki.erply.com/en/article/1720) |
| [Get Address Types](actions/get-address-types.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getaddresstypes) |
| [Get Addresses](actions/get-addresses.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getaddresses) |
| [Get Allowed Warehouses](actions/get-allowed-warehouses.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getallowedwarehouses) |
| [Get Brands](actions/get-brands.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getbrands) |
| [Get Campaigns](actions/get-campaigns.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getcampaigns) |
| [Get Company Info](actions/get-company-info.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getcompanyinfo) |
| [Get Configuration Parameters](actions/get-conf-parameters.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getconfparameters) |
| [Get Countries](actions/get-countries.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getcountries) |
| [Get Currencies](actions/get-currencies.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getcurrencies) |
| [Get Customer Groups](actions/get-customer-groups.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getcustomergroups) |
| [Get Customers](actions/get-customers.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getcustomers) |
| [Get Default Customer](actions/get-default-customer.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getdefaultcustomer) |
| [Get Employees](actions/get-employees.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getemployees) |
| [Get Payment Types](actions/get-payment-types.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getpaymenttypes) |
| [Get Points of Sale](actions/get-points-of-sale.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getpointsofsale) |
| [Get Price Lists](actions/get-price-lists.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getpricelists) |
| [Get Product Categories](actions/get-product-categories.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getproductcategories) |
| [Get Product Groups](actions/get-product-groups.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getproductgroups) |
| [Get Product Priority Groups](actions/get-product-priority-groups.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getproductprioritygroups) |
| [Get Product Stock](actions/get-product-stock.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getproductstock) |
| [Get Product Units](actions/get-product-units.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getproductunits) |
| [Get Products](actions/get-products.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getproducts) |
| [Get Projects](actions/get-projects.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getprojects) |
| [Get Purchase Documents](actions/get-purchase-documents.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getpurchasedocuments) |
| [Get Sales Documents](actions/get-sales-documents.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getsalesdocuments) |
| [Get Services](actions/get-services.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getservices) |
| [Get Suppliers](actions/get-suppliers.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getsuppliers) |
| [Get VAT Rates](actions/get-vat-rates.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getvatrates) |
| [Get Warehouses](actions/get-warehouses.md) | `POST /` | [docs](https://learn-api.erply.com/requests/getwarehouses) |
