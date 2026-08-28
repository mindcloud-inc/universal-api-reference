# Centerpoint: Native API Reference

A consolidated summary of Centerpoint's API configuration and 66 documented operations, with links to official documentation.

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

Send filters in the query string. Supported operators: `eq`, `gt`, `lt`.

## Sorting

Set the sort field with `sort` in the query string. Use `ascending` for ascending order and `-` for descending order. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (66 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST companies` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/companiesPOST) |
| [Create Contact](actions/create-contact.md) | `POST profiles` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/profilesPOST) |
| [Create File](actions/create-file.md) | `POST files` | [docs](https://api.centerpointconnect.io/centerpoint/files) |
| [Create File Upload](actions/create-file-upload.md) | `POST file/url` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/filesPOST) |
| [Create Opportunity](actions/create-opportunity.md) | `GET opportunities` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/opportunitiesPOST) |
| [Create Property](actions/create-property.md) | `POST properties` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/propertiesPOST) |
| [Create Transaction](actions/create-transaction.md) | `POST transactions` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/transactionsPOST) |
| [Get Budget Type](actions/get-budget-type.md) | `GET budget_types/:BUDGET_TYPE_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/budget_types/{BUDGET_TYPE_ID}GET) |
| [Get Building](actions/get-building.md) | `GET buildings/:BUILDING_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/buildings/BUILDING_IDGET) |
| [Get Building Division](actions/get-building-division.md) | `GET building_divisions/:BUILDING_DIVISIONS_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/building_divisions/BUILDING_DIVISIONS_IDGET) |
| [Get Building Outline](actions/get-building-outline.md) | `GET building_outlines/:BUILDING_OUTLINES_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/building_outlines/BUILDING_OUTLINES_IDGET) |
| [Get Building Photo](actions/get-building-photo.md) | `GET building_photos/:BUILDING_PHOTO_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/building_photos/BUILDING_PHOTO_IDGET) |
| [Get Contact](actions/get-contact.md) | `GET profiles/:PROFILE_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/profiles/{PROFILE_ID}GET) |
| [Get Cost Code](actions/get-cost-code.md) | `GET cost_codes/:COST_CODE_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/cost_codes/{COST_CODE_ID}GET) |
| [Get Employee](actions/get-employee.md) | `GET employees/:EMPLOYEE_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/employees/{EMPLOYEE_ID}GET) |
| [Get File](actions/get-file.md) | `GET files/:FILE_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/files/FILE_IDGET) |
| [Get Invoice](actions/get-invoice.md) | `GET invoices/:INVOICE_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/invoices/{INVOICE_ID}GET) |
| [Get Location](actions/get-location.md) | `GET locations/:LOCATION_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/locations/{LOCATION_ID}GET) |
| [Get Material](actions/get-material.md) | `GET materials/:MATERIAL_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/materials/{MATERIAL_ID}GET) |
| [Get Opportunity](actions/get-opportunity.md) | `GET opportunities/:OPPORTUNITY_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/opportunities/{OPPORTUNITY_ID}GET) |
| [Get Product](actions/get-product.md) | `GET products/:PRODUCT_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/products/PRODUCT_IDGET) |
| [Get Product Template](actions/get-product-template.md) | `GET product_templates/:PRODUCT_TEMPLATE_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/product_templates/PRODUCT_TEMPLATE_IDGET) |
| [Get Production Day](actions/get-production-day.md) | `GET production_days/:PRODUCTION_DAYS_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/production_days/PRODUCTION_DAYS_IDGET) |
| [Get Production Item](actions/get-production-item.md) | `GET production_items/:PRODUCTION_ITEM_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/production_items/PRODUCTION_ITEM_IDGET) |
| [Get Service](actions/get-service.md) | `GET services/:SERVICE_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/services/{SERVICE_ID}GET) |
| [Get Service Agreement](actions/get-service-agreement.md) | `GET service_agreements/:SERVICE_AGREEMENT_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/service_agreements/SERVICE_AGREEMENT_IDGET) |
| [Get Company](actions/get-single-company.md) | `GET companies/:COMPANY_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/companies/{COMPANY_ID}GET) |
| [Get Production](actions/get-single-production.md) | `GET productions/:PRODUCTION_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/productions/{PRODUCTION_ID}GET) |
| [Get Property](actions/get-single-property.md) | `GET properties/:PROPERTY_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/properties/{PROPERTY_ID}GET) |
| [Get Task](actions/get-task.md) | `GET tasks/:TASK_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/tasks/TASK_IDGET) |
| [Get Tax Code](actions/get-tax-code.md) | `GET tax_codes/:TAX_CODE_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/tax_codes/{TAX_CODE_ID}GET) |
| [Get Warranty](actions/get-warranty.md) | `GET warranties/:WARRANTY_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/warranties/WARRANTY_IDGET) |
| [Get Work Time Entry](actions/get-work-time-entry.md) | `GET work_time_entries/:WORK_TIME_ENTRIES_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/work_time_entries/WORK_TIME_ENTRIES_IDGET) |
| [List Budget Entries](actions/list-budget-entries.md) | `GET budget` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/budgetGET) |
| [List Budget Types](actions/list-budget-types.md) | `GET budget_types` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/budget_typesGET) |
| [List Companies](actions/list-companies.md) | `GET companies` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/companiesGET) |
| [List Contacts](actions/list-contacts.md) | `GET profiles` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/profilesGET) |
| [List Cost Codes](actions/list-cost-codes.md) | `GET cost_codes` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/cost_codesGET) |
| [List Employees](actions/list-employees.md) | `GET employees` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/employeesGET) |
| [List Files](actions/list-files.md) | `GET files` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/filesGET) |
| [List Invoices](actions/list-invoices.md) | `GET invoices` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/invoicesGET) |
| [List Locations](actions/list-locations.md) | `GET locations` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/locationsGET) |
| [List Materials](actions/list-materials.md) | `GET materials` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/materialsGET) |
| [List Model Files](actions/list-model-files.md) | `GET model_files` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/model_filesGET) |
| [List Opportunities](actions/list-opportunities.md) | `GET opportunities` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/opportunitiesGET) |
| [List Product Template Tags](actions/list-product-template-tags.md) | `GET product_template_tags` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/product_template_tagsGET) |
| [List Product Templates](actions/list-product-templates.md) | `GET product_templates` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/product_templatesGET) |
| [List Production Days](actions/list-production-days.md) | `GET production_days` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/production_daysGET) |
| [List Production Items](actions/list-production-items.md) | `GET production_items` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/production_itemsGET) |
| [List Production Materials](actions/list-production-materials.md) | `GET production_materials` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/production_materialsGET) |
| [List Production Materials by Production](actions/list-production-materials-by-production.md) | `GET productions/:PRODUCTION_ID/production_materials` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/productions/PRODUCTION_ID/production_materialsGET) |
| [List Production Purchase Orders](actions/list-production-purchase-orders.md) | `GET productions/:PRODUCTION_ID/purchase_orders` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/productions/{PRODUCTION_ID}/purchase_ordersGET) |
| [List Productions](actions/list-productions.md) | `GET productions` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/productionsGET) |
| [List Productions With Domain Production Only](actions/list-productions-with-domain-production-only.md) | `GET productions` |  |
| [List Products](actions/list-products.md) | `GET products` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/productsGET) |
| [List Properties](actions/list-properties.md) | `GET properties` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/propertiesGET) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET purchase_orders` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/purchase_ordersGET) |
| [List Service Agreements](actions/list-service-agreements.md) | `GET service_agreements` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/service_agreementsGET) |
| [List Services](actions/list-services.md) | `GET services` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/servicesGET) |
| [List Tasks](actions/list-tasks.md) | `GET tasks` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/tasksGET) |
| [List Tax Codes](actions/list-tax-codes.md) | `GET tax_codes` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/tax_codesGET) |
| [List Warranties](actions/list-warranties.md) | `GET warranties` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/warrantiesGET) |
| [List Work Time Entries](actions/list-work-time-entries.md) | `GET work_time_entries` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/work_time_entriesGET) |
| [Update Company](actions/update-company.md) | `PATCH companies/:COMPANY_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/companies/{COMPANY_ID}PATCH) |
| [Update Invoice](actions/update-invoice.md) | `PATCH invoices/:INVOICE_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/invoices/{INVOICE_ID}PATCH) |
| [Update Property](actions/update-property.md) | `PATCH properties/:PROPERTY_ID` | [docs](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/properties/%7BPROPERTY_ID%7DPATCH) |
