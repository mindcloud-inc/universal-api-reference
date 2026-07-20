# Oboloo: Native API Reference

A consolidated summary of Oboloo's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://oboloo.app/api/documentation
- **OpenAPI specification:** https://oboloo.app/docs/api-docs.json
- **API base URL:** `https://mindcloudwizard20260330.oboloo.app/api`

## Authentication

### API Key

Connect to Oboloo with a tenant-scoped API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.oboloo.com/en/creating-and-testing-api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `totalPage`. The current page number is read from `page`.

## Pagination

Use `itemsPerPage` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contract Document Type](actions/create-contract-document-type.md) | `POST /configuration/add-contract-document-Types` | [docs](https://oboloo.app/api/documentation) |
| [Create Contract Type](actions/create-contract-type.md) | `POST /configuration/add-contract-type` | [docs](https://oboloo.app/api/documentation) |
| [Create Industry](actions/create-industry.md) | `POST /configuration/addIndustry` | [docs](https://oboloo.app/api/documentation) |
| [Create Payment Term](actions/create-payment-term.md) | `POST /configuration/addpaymentTerms` | [docs](https://oboloo.app/api/documentation) |
| [Create Saving Type](actions/create-saving-type.md) | `POST /configuration/add-saving-type` | [docs](https://oboloo.app/api/documentation) |
| [Create Subcategory](actions/create-subcategory.md) | `POST /configuration/addSubCategory` | [docs](https://oboloo.app/api/documentation) |
| [Create Subindustry](actions/create-subindustry.md) | `POST /configuration/addsubIndustry` | [docs](https://oboloo.app/api/documentation) |
| [Create Supplier Document Type](actions/create-supplier-document-type.md) | `POST /configuration/add-suppliers-document-Types` | [docs](https://oboloo.app/api/documentation) |
| [Create Supplier Type](actions/create-supplier-type.md) | `POST /configuration/add-supplier-Types` | [docs](https://oboloo.app/api/documentation) |
| [List Active Currencies](actions/list-active-currencies.md) | `GET /currency-rates/get-all-active-currency` | [docs](https://oboloo.app/api/documentation) |
| [List Categories](actions/list-categories.md) | `GET /configuration/getCategories` | [docs](https://oboloo.app/api/documentation) |
| [List Contract Document Types](actions/list-contract-document-types.md) | `GET /configuration/get-contract-document-Types` | [docs](https://oboloo.app/api/documentation) |
| [List Contract Types](actions/list-contract-types.md) | `GET /configuration/contract-type-list` | [docs](https://oboloo.app/api/documentation) |
| [List Industries](actions/list-industries.md) | `GET /configuration/getIndustries` | [docs](https://oboloo.app/api/documentation) |
| [List Payment Terms](actions/list-payment-terms.md) | `GET /configuration/getpaymentTerms` | [docs](https://oboloo.app/api/documentation) |
| [List Saving Types](actions/list-saving-types.md) | `GET /configuration/saving-type-list` | [docs](https://oboloo.app/api/documentation) |
| [List Subcategories](actions/list-subcategories.md) | `GET /configuration/getAllSubCategories` | [docs](https://oboloo.app/api/documentation) |
| [List Subindustries](actions/list-subindustries.md) | `GET /configuration/getSubIndustries` | [docs](https://oboloo.app/api/documentation) |
| [List Supplier Document Types](actions/list-supplier-document-types.md) | `GET /configuration/get-suppliers-document-Types` | [docs](https://oboloo.app/api/documentation) |
| [List Supplier Types](actions/list-supplier-types.md) | `GET /configuration/get-supplier-Types` | [docs](https://oboloo.app/api/documentation) |
