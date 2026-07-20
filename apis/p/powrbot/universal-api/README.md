# <img src="https://images.mindcloud.co/apps/icons/powrbot_1776089675540.png" alt="Powrbot logo" width="28" height="28"> Powrbot: Universal API

Search and enrich company records with public web data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/powrbot/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://powrbot.com/
- **Vendor API docs:** https://powrbot.com/cpages/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Company](actions/search-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/search-company?connectionId=$CONNECTION_ID&company=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Search Company](actions/search-company.md) | GET | Finds a company in Powrbot by company name. |

### Search Csv

| Action | Method | Description |
| --- | --- | --- |
| [Download Search CSV](actions/download-search-csv.md) | GET | Retrieves CSV output for a Powrbot bulk search. |

### Search Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Search](actions/get-search.md) | GET | Retrieves a bulk search job from Powrbot. |
| [List Searches](actions/list-searches.md) | GET | Retrieves bulk search jobs from Powrbot. |
| [Start Bulk Search](actions/start-bulk-search.md) | POST | Creates a bulk search job in Powrbot. |

