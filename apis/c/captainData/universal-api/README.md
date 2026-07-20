# <img src="https://images.mindcloud.co/apps/icons/captain-data-icon_1775848244316.png" alt="Captain Data logo" width="28" height="28"> Captain Data: Universal API

Captain Data API integration for workspace quotas, people enrichment and search, company enrichment and search, and related Captain Data automation endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/captainData/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.captaindata.com
- **Vendor API docs:** https://docs.captaindata.com/v1/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Quotas](actions/get-quotas.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captainData/latest/actions/get-quotas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Company](actions/enrich-company.md) | GET | Retrieves detailed company data from Captain Data by LinkedIn URL. |
| [Find Company](actions/find-company.md) | GET | Finds a company in Captain Data by company name. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Captain Data by Sales Navigator query. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Enrich People](actions/enrich-people.md) | GET | Retrieves detailed person data from Captain Data by LinkedIn URL. |
| [Find People](actions/find-people.md) | GET | Finds a person in Captain Data by full name. |
| [Search People](actions/search-people.md) | GET | Finds people in Captain Data by Sales Navigator query. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Find Company Employees](actions/find-company-employees.md) | GET | Finds company employees in Captain Data by company UID. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Quotas](actions/get-quotas.md) | GET | Retrieves workspace quota details from Captain Data. |

