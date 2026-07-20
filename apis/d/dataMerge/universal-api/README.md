# <img src="https://images.mindcloud.co/apps/icons/datamerge_1781650430593.png" alt="DataMerge logo" width="28" height="28"> DataMerge: Universal API

DataMerge: Enrich companies, search contacts, and explore corporate hierarchies

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dataMerge/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.datamerge.ai
- **Vendor API docs:** https://api.datamerge.ai/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits Balance](actions/get-credits-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/get-credits-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits Balance](actions/get-credits-balance.md) | GET | Retrieves your current credit balance from DataMerge. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Companies](actions/enrich-companies.md) | POST | Starts a DataMerge company enrichment job from one or more domains. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from DataMerge by DataMerge ID or record ID. |
| [Search Lookalike Companies](actions/search-lookalike-companies.md) | POST |  |

### Company Enrichment Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Enrichment Status](actions/get-company-enrichment-status.md) | GET | Retrieves a DataMerge company enrichment job status. |

### Company Hierarchy

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Hierarchy](actions/get-company-hierarchy.md) | GET | Retrieves a company hierarchy from DataMerge by DataMerge ID. |

### Company Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Webhook Example](actions/get-company-webhook-example.md) | GET | Retrieves the company webhook payload example from DataMerge. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Contacts](actions/enrich-contacts.md) | POST | Starts a DataMerge contact enrichment job. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from DataMerge by record ID. |
| [Search Contacts](actions/search-contacts.md) | POST | Starts a DataMerge contact search by company and filters. |

### Contact Enrichment Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Enrichment Status](actions/get-contact-enrichment-status.md) | GET | Retrieves a DataMerge contact enrichment job status. |

### Contact Search Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Search Status](actions/get-contact-search-status.md) | GET | Retrieves a DataMerge contact search job status. |

### Contact Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Webhook Example](actions/get-contact-webhook-example.md) | GET | Retrieves the contact webhook payload example from DataMerge. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Add Items to List](actions/add-items-to-list.md) | PUT | Adds companies or contacts to a DataMerge list. |
| [Create List](actions/create-list.md) | POST | Creates a new company or contact list in DataMerge. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing list from DataMerge. |
| [Get Lists](actions/get-lists.md) | GET | Retrieves company or contact lists from DataMerge. |

### List Item

| Action | Method | Description |
| --- | --- | --- |
| [Move Item To Another List](actions/move-item-to-another-list.md) | PUT | Moves an item to another DataMerge list. |
| [Remove Item From List](actions/remove-item-from-list.md) | DELETE | Removes an item from a DataMerge list. |

### List Member

| Action | Method | Description |
| --- | --- | --- |
| [Get List Members](actions/get-list-members.md) | GET | Retrieves items from a specific DataMerge list. |

### Lookalike Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Lookalike Company Status](actions/get-lookalike-company-status.md) | GET |  |

