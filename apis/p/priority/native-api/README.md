# Priority: Native API Reference

A consolidated summary of Priority's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://prioritysoftware.github.io/restapi/
- **API base URL:** `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`

## Authentication

### Basic Auth

Use the official Priority sandbox or tenant username and password for HTTP Basic authentication.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://prioritysoftware.github.io/restapi/authenticate/)

## Pagination

Use `$top` in the query string to set the page size (default 50; minimum 1). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`, `ge`, `gt`, `le`, `lt`, `ne`.

## Sorting

Set the sort field with `$orderby` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get AP Invoice](actions/get-ap-invoice.md) | `GET /PINVOICES(IVNUM=':ivNum',DEBIT=':debit',IVTYPE=':ivType')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get AR Invoice](actions/get-ar-invoice.md) | `GET /AINVOICES(IVNUM=':ivNum',DEBIT=':debit',IVTYPE=':ivType')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Bank](actions/get-bank.md) | `GET /BANKS(BANKCODE=':bankCode')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Company](actions/get-company.md) | `GET /COMPANIES(COMPANYNAME=':companyName')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Country](actions/get-country.md) | `GET /COUNTRIES(COUNTRYNAME=':countryName')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Currency](actions/get-currency.md) | `GET /CURRENCIES(CODE=':code')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Customer](actions/get-customer.md) | `GET /CUSTOMERS(CUSTNAME=':custName')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Customer Document](actions/get-customer-document.md) | `GET /DOCUMENTS_C(DOCNO=':docNo',TYPE=':type')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Document Type](actions/get-document-type.md) | `GET /DOCTYPES(TYPE=':type')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Login Name](actions/get-login-name.md) | `GET /GetLoginName()` | [docs](https://prioritysoftware.github.io/restapi/request/) |
| [Get OData Version](actions/get-o-data-version.md) | `GET /GetODataVersion()` | [docs](https://prioritysoftware.github.io/restapi/request/#Request_Priority_Version) |
| [Get Part](actions/get-part.md) | `GET /PART(PARTNAME=':partName')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Part Balance](actions/get-part-balance.md) | `GET /PARTBAL(WARHS=:warhs,PART=:part,CUST=:cust,ACT=:act,SERIAL=:serial)` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Priority Version](actions/get-priority-version.md) | `GET /GetPriorityVersion()` | [docs](https://prioritysoftware.github.io/restapi/request/#Request_Priority_Version) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /PORDERS(ORDNAME=':ordName')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Quotation Document](actions/get-quotation-document.md) | `GET /DOCUMENTS_Q(DOCNO=':docNo',TYPE=':type')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /ORDERS(ORDNAME=':ordName')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Shipper](actions/get-shipper.md) | `GET /SHIPPERS(SHIPPERNAME=':shipperName')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Supplier](actions/get-supplier.md) | `GET /SUPPLIERS(SUPNAME=':supName')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Tenant Details](actions/get-tenant-details.md) | `GET /GetTenantDetails()` | [docs](https://prioritysoftware.github.io/restapi/request/) |
| [Get User](actions/get-user.md) | `GET /USERS(USERLOGIN=':userLogin')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [Get Warehouse](actions/get-warehouse.md) | `GET /WAREHOUSES(WARHSNAME=':warhsName',LOCNAME=':locName')` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_an_Individual_Entity_by_ID) |
| [List AP Invoices](actions/list-ap-invoices.md) | `GET /PINVOICES` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List AR Invoices](actions/list-ar-invoices.md) | `GET /AINVOICES` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Banks](actions/list-banks.md) | `GET /BANKS` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Companies](actions/list-companies.md) | `GET /COMPANIES` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Countries](actions/list-countries.md) | `GET /COUNTRIES` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Currencies](actions/list-currencies.md) | `GET /CURRENCIES` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Customer Documents](actions/list-customer-documents.md) | `GET /DOCUMENTS_C` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Customers](actions/list-customers.md) | `GET /CUSTOMERS` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Document Types](actions/list-document-types.md) | `GET /DOCTYPES` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Part Balances](actions/list-part-balances.md) | `GET /PARTBAL` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Parts](actions/list-parts.md) | `GET /PART` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /PORDERS` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Quotation Documents](actions/list-quotation-documents.md) | `GET /DOCUMENTS_Q` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /ORDERS` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Shippers](actions/list-shippers.md) | `GET /SHIPPERS` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Suppliers](actions/list-suppliers.md) | `GET /SUPPLIERS` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Users](actions/list-users.md) | `GET /USERS` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
| [List Warehouses](actions/list-warehouses.md) | `GET /WAREHOUSES` | [docs](https://prioritysoftware.github.io/restapi/request/#Requesting_Entity_Collections) |
