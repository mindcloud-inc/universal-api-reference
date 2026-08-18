# <img src="https://images.mindcloud.co/apps/icons/cropped-centerpoint-favicon_1768252732718.png" alt="Centerpoint logo" width="28" height="28"> Centerpoint: Universal API

Centerpoint through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/centerpoint/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.centerpointconnect.com/
- **Vendor API docs:** https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get cost_code](actions/get-cost-code.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-cost-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [Get Single Company](actions/get-single-company.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Cost Code

| Action | Method | Description |
| --- | --- | --- |
| [Get cost_code](actions/get-cost-code.md) | GET |  |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [List Productions_items](actions/list-productions-items.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST |  |
| [Create File Upload](actions/create-file-upload.md) | POST |  |
| [Get Single File](actions/get-single-file.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [Update Invoice](actions/update-invoice.md) | PUT |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Single Production](actions/get-single-production.md) | GET |  |
| [List Productions](actions/list-productions.md) | GET |  |
| [List Productions With Domain Production Only](actions/list-productions-with-domain-production-only.md) | GET |  |

### Model_files

| Action | Method | Description |
| --- | --- | --- |
| [List Model Files](actions/list-model-files.md) | GET |  |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity](actions/create-opportunity.md) | POST |  |
| [List Opportunities](actions/list-opportunities.md) | GET |  |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Property](actions/create-property.md) | POST |  |
| [Get Single Property](actions/get-single-property.md) | GET |  |
| [List Properties](actions/list-properties.md) | GET |  |
| [Update Property](actions/update-property.md) | PUT |  |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [List Services](actions/list-services.md) | GET |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST |  |

