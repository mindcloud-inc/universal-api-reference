# <img src="https://images.mindcloud.co/apps/icons/pipedrive_1772738753904.png" alt="Pipedrive logo" width="28" height="28"> Pipedrive: Universal API

Manage deals, activities, contacts, and sales pipelines

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pipedrive/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pipedrive.com
- **Vendor API docs:** https://developers.pipedrive.com/docs/api/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Activities](actions/get-activities.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Add Activity](actions/add-activity.md) | POST | Creates a new activity in Pipedrive. |
| [Delete Activity](actions/delete-activity.md) | DELETE | Deletes an existing activity from Pipedrive. |
| [Get Activities](actions/get-activities.md) | GET | Retrieves activities from Pipedrive. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an existing activity in Pipedrive. |

### Custom Fields Of A Deal

| Action | Method | Description |
| --- | --- | --- |
| [Get All Deal Fields](actions/get-all-deal-fields.md) | GET | Retrieves deal fields from Pipedrive. |

### Custom Fields Of A Product

| Action | Method | Description |
| --- | --- | --- |
| [Get All Product Fields](actions/get-all-deal-fields-copy.md) | GET | Retrieves product fields from Pipedrive. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Add Deal](actions/add-deal.md) | POST | Creates a new deal in Pipedrive. |
| [Convert Deal To Lead](actions/convert-deal-to-lead.md) | PUT | Converts a deal to a lead in Pipedrive. |
| [Convert Lead To Deal](actions/convert-lead-to-deal.md) | POST | Converts a lead to a deal in Pipedrive. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes an existing deal from Pipedrive. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a deal from Pipedrive. |
| [Get Deals Summary](actions/get-deals-summary.md) | GET | Retrieves deal summary metrics from Pipedrive. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deals from Pipedrive. |
| [Search Deals](actions/search-deals.md) | GET | Finds deals in Pipedrive by search term. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in Pipedrive. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Add Lead](actions/add-lead.md) | POST | Creates a new lead in Pipedrive. |
| [Get Leads](actions/get-leads.md) | GET | Retrieves leads from Pipedrive. |
| [Search Leads](actions/search-leads.md) | GET | Finds leads in Pipedrive by search term. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Add Organization](actions/add-organization.md) | POST | Creates a new organization in Pipedrive. |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Pipedrive. |
| [Get Organizations](actions/get-organizations.md) | GET | Retrieves organizations from Pipedrive. |
| [Search Organizations](actions/search-organization.md) | GET | Finds organizations in Pipedrive by search term. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in Pipedrive. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Add Person](actions/add-person.md) | POST | Creates a new person in Pipedrive. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from Pipedrive. |
| [Get Persons](actions/get-persons.md) | GET | Retrieves person records from Pipedrive. |
| [Search Persons](actions/search-persons.md) | GET | Finds people in Pipedrive by search term. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in Pipedrive. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Add Product](actions/add-product.md) | POST | Creates a new product in Pipedrive. |
| [Get Products](actions/get-products.md) | GET | Retrieves products from Pipedrive. |
| [Search Products](actions/search-products.md) | GET | Finds products in Pipedrive by search term. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Add Product to Deal](actions/add-product-to-deal.md) | POST | Adds a product to a deal in Pipedrive. |
| [Update a Product](actions/update-a-product.md) | PUT | Updates an existing product in Pipedrive. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Add Webhook](actions/add-webhook.md) | POST | Creates a new webhook in Pipedrive. |

