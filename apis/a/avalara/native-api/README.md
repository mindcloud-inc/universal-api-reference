# Avalara AvaTax: Native API Reference

A consolidated summary of Avalara AvaTax's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.avalara.com/api-reference/avatax/rest/v2/methods/
- **API base URL:** `{environment}`

## Authentication

### Basic

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Environment:** `environment` · required · AvaTax REST base URL. Sandbox: https://sandbox-rest.avatax.com/api/v2/. Production: https://rest.avatax.com/api/v2/.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.avalara.com/avatax/authentication-in-rest/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The next-page cursor is read from `pageKey`.

## Pagination

Use `$top` in the query string to set the page size (maximum 1000). Use `$skip` in the query string as the record offset.

## Filtering

Send filters in the query string. Supported operators: `between`, `contains`, `endswith`, `eq`, `ge`, `gt`, `in`, `le`, `lt`, `ne`, `startswith`.

## Sorting

Set the sort field with `$orderBy` in the query string. Multiple sort fields can be combined.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | `POST transactions/create` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Transactions/CreateTransaction/) |
| [Get Company](actions/get-company.md) | `GET companies/:id` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Companies/GetCompany/) |
| [Get Customer](actions/get-customer.md) | `GET companies/:companyId/customers/:customerCode` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Customers/GetCustomer/) |
| [Get Item](actions/get-item.md) | `GET companies/:companyId/items/:id` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Items/GetItem/) |
| [Get Nexus](actions/get-nexus.md) | `GET companies/:companyId/nexus/:id` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Nexus/GetNexus/) |
| [Get Tax Code](actions/get-tax-code.md) | `GET companies/:companyId/taxcodes/:id` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/TaxCodes/GetTaxCode/) |
| [Get Transaction By Code](actions/get-transaction-by-code.md) | `GET companies/:companyCode/transactions/:transactionCode` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Transactions/GetTransactionByCode/) |
| [Get Transaction By Id](actions/get-transaction-by-id.md) | `GET transactions/:id` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Transactions/GetTransactionById/) |
| [List Countries](actions/list-countries.md) | `GET definitions/countries` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Definitions/ListCountries/) |
| [List Currencies](actions/list-currencies.md) | `GET definitions/currencies` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Definitions/ListCurrencies/) |
| [List Entity Use Codes](actions/list-entity-use-codes.md) | `GET definitions/entityusecodes` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Definitions/ListEntityUseCodes/) |
| [List Items By Company](actions/list-items-by-company.md) | `GET companies/:companyId/items` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Items/ListItemsByCompany/) |
| [List Jurisdictions Hierarchy](actions/list-jurisdictions-hierarchy.md) | `GET definitions/jurisdictions` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Definitions/ListJurisdictionsHierarchy/) |
| [List Nexus By Company](actions/list-nexus-by-company.md) | `GET companies/:companyId/nexus` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Nexus/ListNexusByCompany/) |
| [List Parameters](actions/list-parameters.md) | `GET definitions/parameters` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Definitions/ListParameters/) |
| [List Tax Authority Types](actions/list-tax-authority-types.md) | `GET definitions/taxauthoritytypes` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Definitions/ListTaxAuthorityTypes/) |
| [List Tax Code Types](actions/list-tax-code-types.md) | `GET definitions/taxcodetypes` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Definitions/ListTaxCodeTypes/) |
| [List Tax Codes By Company](actions/list-tax-codes-by-company.md) | `GET companies/:companyId/taxcodes` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/TaxCodes/ListTaxCodesByCompany/) |
| [List Tax Rules](actions/list-tax-rules.md) | `GET taxrules` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/TaxRules/ListTaxRules/) |
| [List Transactions By Company](actions/list-transactions-by-company.md) | `GET companies/:companyCode/transactions` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Transactions/ListTransactionsByCompany/) |
| [Query Companies](actions/query-companies.md) | `GET companies` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Companies/QueryCompanies/) |
| [Query Customers](actions/query-customers.md) | `GET companies/:companyId/customers` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Customers/QueryCustomers/) |
| [Query Tax Codes](actions/query-tax-codes.md) | `GET taxcodes` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/TaxCodes/QueryTaxCodes/) |
| [Test Connection](actions/test-connection.md) | `GET utilities/ping` | [docs](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Utilities/Ping/) |
