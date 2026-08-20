# <img src="https://images.mindcloud.co/apps/icons/cropped-centerpoint-favicon_1768252732718.png" alt="Centerpoint logo" width="28" height="28"> Centerpoint: Universal API

Centerpoint through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/centerpoint/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 65
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.centerpointconnect.com/
- **Vendor API docs:** https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Budget Type](actions/get-budget-type.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-budget-type?connectionId=$CONNECTION_ID&BUDGET_TYPE_ID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (65)

### Budget Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Budget Entries](actions/list-budget-entries.md) | GET |  |

### Budget Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Budget Type](actions/get-budget-type.md) | GET |  |
| [List Budget Types](actions/list-budget-types.md) | GET |  |

### Building

| Action | Method | Description |
| --- | --- | --- |
| [Get Building](actions/get-building.md) | GET |  |

### Building Division

| Action | Method | Description |
| --- | --- | --- |
| [Get Building Division](actions/get-building-division.md) | GET |  |

### Building Outline

| Action | Method | Description |
| --- | --- | --- |
| [Get Building Outline](actions/get-building-outline.md) | GET |  |

### Building Photo

| Action | Method | Description |
| --- | --- | --- |
| [Get Building Photo](actions/get-building-photo.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [Get Company](actions/get-single-company.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Cost Code

| Action | Method | Description |
| --- | --- | --- |
| [Get Cost Code](actions/get-cost-code.md) | GET |  |
| [List Cost Codes](actions/list-cost-codes.md) | GET |  |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee](actions/get-employee.md) | GET |  |
| [List Employees](actions/list-employees.md) | GET |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET |  |
| [List Files](actions/list-files.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST |  |
| [Create File Upload](actions/create-file-upload.md) | POST |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Update Invoice](actions/update-invoice.md) | PUT |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [List Productions With Domain Production Only](actions/list-productions-with-domain-production-only.md) | GET |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET |  |
| [List Locations](actions/list-locations.md) | GET |  |

### Material

| Action | Method | Description |
| --- | --- | --- |
| [Get Material](actions/get-material.md) | GET |  |
| [List Materials](actions/list-materials.md) | GET |  |

### Model File

| Action | Method | Description |
| --- | --- | --- |
| [List Model Files](actions/list-model-files.md) | GET |  |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity](actions/create-opportunity.md) | POST |  |
| [Get Opportunity](actions/get-opportunity.md) | GET |  |
| [List Opportunities](actions/list-opportunities.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |

### Product Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Template](actions/get-product-template.md) | GET |  |
| [List Product Templates](actions/list-product-templates.md) | GET |  |

### Product Template Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Product Template Tags](actions/list-product-template-tags.md) | GET |  |

### Production

| Action | Method | Description |
| --- | --- | --- |
| [Get Production](actions/get-single-production.md) | GET |  |
| [List Productions](actions/list-productions.md) | GET |  |

### Production Day

| Action | Method | Description |
| --- | --- | --- |
| [Get Production Day](actions/get-production-day.md) | GET |  |
| [List Production Days](actions/list-production-days.md) | GET |  |

### Production Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Production Item](actions/get-production-item.md) | GET |  |
| [List Production Items](actions/list-production-items.md) | GET |  |

### Production Material

| Action | Method | Description |
| --- | --- | --- |
| [List Production Materials](actions/list-production-materials.md) | GET |  |
| [List Production Materials by Production](actions/list-production-materials-by-production.md) | GET |  |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Property](actions/create-property.md) | POST |  |
| [Get Property](actions/get-single-property.md) | GET |  |
| [List Properties](actions/list-properties.md) | GET |  |
| [Update Property](actions/update-property.md) | PUT |  |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [List Production Purchase Orders](actions/list-production-purchase-orders.md) | GET |  |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET |  |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Service](actions/get-service.md) | GET |  |
| [List Services](actions/list-services.md) | GET |  |

### Service Agreement

| Action | Method | Description |
| --- | --- | --- |
| [Get Service Agreement](actions/get-service-agreement.md) | GET |  |
| [List Service Agreements](actions/list-service-agreements.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |

### Tax Code

| Action | Method | Description |
| --- | --- | --- |
| [Get Tax Code](actions/get-tax-code.md) | GET |  |
| [List Tax Codes](actions/list-tax-codes.md) | GET |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST |  |

### Warranty

| Action | Method | Description |
| --- | --- | --- |
| [Get Warranty](actions/get-warranty.md) | GET |  |
| [List Warranties](actions/list-warranties.md) | GET |  |

### Work Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Work Time Entry](actions/get-work-time-entry.md) | GET |  |
| [List Work Time Entries](actions/list-work-time-entries.md) | GET |  |

