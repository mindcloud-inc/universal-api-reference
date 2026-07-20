# <img src="https://images.mindcloud.co/apps/icons/68db9914a8adc6265028bb3b-reverse-o-logo-very_1774907077370.png" alt="Oboloo logo" width="28" height="28"> Oboloo: Universal API

Cloud procurement platform for supplier management, sourcing, contract management, and savings management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oboloo/latest
- **Category:** Commerce / Procurement
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://oboloo.com/
- **Vendor API docs:** https://oboloo.app/api/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Categories](actions/list-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Oboloo. |

### Contract Document Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract Document Type](actions/create-contract-document-type.md) | POST | Creates a new contract document type in Oboloo. |
| [List Contract Document Types](actions/list-contract-document-types.md) | GET | Retrieves contract document types from Oboloo. |

### Contract Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract Type](actions/create-contract-type.md) | POST | Creates a new contract type in Oboloo. |
| [List Contract Types](actions/list-contract-types.md) | GET | Retrieves contract types from Oboloo. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Active Currencies](actions/list-active-currencies.md) | GET | Retrieves active currencies from Oboloo. |

### Industry

| Action | Method | Description |
| --- | --- | --- |
| [Create Industry](actions/create-industry.md) | POST | Creates a new industry in Oboloo. |
| [List Industries](actions/list-industries.md) | GET | Retrieves industries from Oboloo. |

### Payment Term

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Term](actions/create-payment-term.md) | POST | Creates a new payment term in Oboloo. |
| [List Payment Terms](actions/list-payment-terms.md) | GET | Retrieves payment terms from Oboloo. |

### Saving Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Saving Type](actions/create-saving-type.md) | POST | Creates a new saving type in Oboloo. |
| [List Saving Types](actions/list-saving-types.md) | GET | Retrieves saving types from Oboloo. |

### Subcategory

| Action | Method | Description |
| --- | --- | --- |
| [Create Subcategory](actions/create-subcategory.md) | POST | Creates a new subcategory in Oboloo. |
| [List Subcategories](actions/list-subcategories.md) | GET | Retrieves subcategories from Oboloo. |

### Subindustry

| Action | Method | Description |
| --- | --- | --- |
| [Create Subindustry](actions/create-subindustry.md) | POST | Creates a new subindustry in Oboloo. |
| [List Subindustries](actions/list-subindustries.md) | GET | Retrieves subindustries from Oboloo. |

### Supplier Document Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier Document Type](actions/create-supplier-document-type.md) | POST | Creates a new supplier document type in Oboloo. |
| [List Supplier Document Types](actions/list-supplier-document-types.md) | GET | Retrieves supplier document types from Oboloo. |

### Supplier Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier Type](actions/create-supplier-type.md) | POST | Creates a new supplier type in Oboloo. |
| [List Supplier Types](actions/list-supplier-types.md) | GET | Retrieves supplier types from Oboloo. |

