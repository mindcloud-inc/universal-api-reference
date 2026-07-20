# <img src="https://images.mindcloud.co/apps/icons/company-hub_1774641140034.png" alt="CompanyHub logo" width="28" height="28"> CompanyHub: Universal API

Manage contacts, companies, deals, and custom CRM records

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/companyHub/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://companyhub.com
- **Vendor API docs:** https://companyhub.com/docs/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in a CompanyHub table. |
| [Delete Records](actions/delete-records.md) | DELETE | Deletes one or more records from a CompanyHub table. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from a specific CompanyHub table. |
| [List Records](actions/list-records.md) | GET | Retrieves records from a specific CompanyHub table. |
| [Search Records](actions/search-records.md) | GET | Finds records in CompanyHub by broad text search. |
| [Search Records by Exact Match](actions/search-records-by-exact-match.md) | GET | Finds records in CompanyHub by exact field criteria. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in a CompanyHub table. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from CompanyHub. |

