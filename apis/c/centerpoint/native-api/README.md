# Centerpoint: Native API Reference

A consolidated summary of Centerpoint's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1
- **API base URL:** `https://api.centerpointconnect.io/centerpoint/`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Header:** `header` · optional

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.centerpointe/authorize to approve access.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.page.total`. The current page number is read from `meta.page.currentPage`.

## Pagination

Use `page[size]` in the query string to set the page size (default 25). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST companies` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/companiesPOST) |
| [Create Contact](actions/create-contact.md) | `POST profiles` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/profilesPOST) |
| [Create File](actions/create-file.md) | `POST files` | [docs](https://api.centerpointconnect.io/centerpoint/files) |
| [Create File Upload](actions/create-file-upload.md) | `POST file/url` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/filesPOST) |
| [Create Opportunity](actions/create-opportunity.md) | `GET opportunities` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/opportunitiesPOST) |
| [Create Property](actions/create-property.md) | `POST properties` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/propertiesPOST) |
| [Create Transaction](actions/create-transaction.md) | `POST transactions` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/transactionsPOST) |
| [Get cost_code](actions/get-cost-code.md) | `GET cost_codes` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/budgetGET) |
| [Get Invoice](actions/get-invoice.md) | `GET invoices/:invoice_id` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/invoices/{INVOICE_ID}GET) |
| [Get Single Company](actions/get-single-company.md) | `GET companies/:COMPANY_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/companiesGET) |
| [Get Single File](actions/get-single-file.md) | `GET files/:fileId` | [docs](https://api.centerpointconnect.io/centerpoint/files) |
| [Get Single Production](actions/get-single-production.md) | `GET productions/:PRODUCTION_ID?include=availableTransitions,availableTransitions.fromStage,availableTransitions.toStage` |  |
| [Get Single Property](actions/get-single-property.md) | `GET properties/:PROPERTYID` | [docs](http://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/propertiesGET) |
| [List Companies](actions/list-companies.md) | `GET companies` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/companiesGET) |
| [List Contacts](actions/list-contacts.md) | `GET profiles` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/propertiesGET) |
| [List Model Files](actions/list-model-files.md) | `GET model_files` | [docs](https://api.centerpointconnect.io/centerpoint/model_files) |
| [List Opportunities](actions/list-opportunities.md) | `GET opportunities` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/opportunitiesGET) |
| [List Productions](actions/list-productions.md) | `GET productions` |  |
| [List Productions_items](actions/list-productions-items.md) | `GET production_items` |  |
| [List Productions With Domain Production Only](actions/list-productions-with-domain-production-only.md) | `GET productions` |  |
| [List Properties](actions/list-properties.md) | `GET properties` | [docs](http://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/propertiesGET) |
| [List Services](actions/list-services.md) | `GET services` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/servicesGET) |
| [Update Invoice](actions/update-invoice.md) | `PATCH invoices/:INVOICE_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/invoices/{INVOICE_ID}PATCH) |
| [Update Property](actions/update-property.md) | `PATCH properties/:PROPERTY_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/properties/%7BPROPERTY_ID%7DPATCH) |
