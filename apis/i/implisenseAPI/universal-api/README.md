# <img src="https://images.mindcloud.co/apps/icons/33babbf4-122d-4aab-86d2-bc31933de3cc-0_1776441411434.png" alt="Implisense logo" width="28" height="28"> Implisense: Universal API

Search German companies and retrieve company, financial, and event data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/implisenseAPI/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://implisense.com/en/products/german-company-data-api
- **Vendor API docs:** https://docs.implisense.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Lookup Companies](actions/lookup-companies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/lookup-companies?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Data](actions/get-company-data.md) | GET | Retrieves company data from Implisense API. |
| [Get Company Data By Lookup](actions/get-company-data-by-lookup.md) | GET | Finds company data in Implisense API by lookup. |
| [Lookup Companies](actions/lookup-companies.md) | GET | Finds companies in Implisense API by known attributes. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Implisense API with filters and facets. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Events](actions/get-company-events.md) | GET | Retrieves company events from Implisense API. |
| [Get Company Events By Lookup](actions/get-company-events-by-lookup.md) | GET | Finds company events in Implisense API by lookup. |

### Financial Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Financials Availability](actions/get-company-financials-availability.md) | GET | Retrieves available financial years from Implisense API. |
| [Get Company Financials Availability By Lookup](actions/get-company-financials-availability-by-lookup.md) | GET | Finds available financial years in Implisense API by lookup. |

### Financials

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Financials](actions/get-company-financials.md) | GET | Retrieves company financials from Implisense API. |
| [Get Company Financials By Lookup](actions/get-company-financials-by-lookup.md) | GET | Finds company financials in Implisense API by lookup. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Jobs](actions/get-company-jobs.md) | GET | Retrieves company jobs from Implisense API. |
| [Get Company Jobs By Lookup](actions/get-company-jobs-by-lookup.md) | GET | Finds company jobs in Implisense API by lookup. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Company People](actions/get-company-people.md) | GET | Retrieves company people from Implisense API. |
| [Get Company People By Lookup](actions/get-company-people-by-lookup.md) | GET | Finds company people in Implisense API by lookup. |

### Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Get Suggestions](actions/get-suggestions.md) | GET | Finds suggestions in Implisense API by prefix. |

