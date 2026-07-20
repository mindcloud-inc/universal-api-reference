# <img src="https://images.mindcloud.co/apps/icons/salescamp_1775060326520.png" alt="Salescamp logo" width="28" height="28"> Salescamp: Universal API

Manage contacts, deals, and sales activity in Salescamp

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salescamp/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.salescamp.app/
- **Vendor API docs:** https://developer.salescamp.app/reference/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Collections](actions/list-collections.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Add Activity to Item](actions/add-activity-to-item.md) | POST |  |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Collections](actions/list-collections.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [Get Company](actions/get-company.md) | GET |  |
| [Update Company](actions/update-company.md) | PUT |  |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST |  |
| [Get Deal](actions/get-deal.md) | GET |  |
| [Update Deal](actions/update-deal.md) | PUT |  |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST |  |
| [Get Item](actions/get-item.md) | GET |  |
| [Update Item](actions/update-item.md) | PUT |  |

