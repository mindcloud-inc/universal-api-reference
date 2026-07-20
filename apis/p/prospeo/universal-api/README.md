# <img src="https://images.mindcloud.co/apps/icons/prospeo_1778083812290.png" alt="Prospeo logo" width="28" height="28"> Prospeo: Universal API

Find, enrich, and sync B2B leads and company data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/prospeo/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://prospeo.io
- **Vendor API docs:** https://prospeo.io/api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Bulk Enrich Companies](actions/bulk-enrich-companies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/bulk-enrich-companies?connectionId=$CONNECTION_ID&data%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Account Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET | Retrieves account information from Prospeo. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Enrich Companies](actions/bulk-enrich-companies.md) | GET | Retrieves enriched company data from Prospeo in bulk. |
| [Enrich Company](actions/enrich-company.md) | GET | Retrieves enriched company data from Prospeo. |
| [Enrich Company by Search Result ID](actions/enrich-company-by-search-result-id.md) | GET | Retrieves enriched company data from Prospeo by search result ID. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Prospeo. |
| [Search Companies by Company List](actions/search-companies-by-company-list.md) | GET | Finds companies in Prospeo by company list. |
| [Search Companies by Funding and Growth](actions/search-companies-by-funding-and-growth.md) | GET | Finds companies in Prospeo by funding and growth. |
| [Search Companies by Industry and Headcount](actions/search-companies-by-industry-and-headcount.md) | GET | Finds companies in Prospeo by industry and headcount. |
| [Search Companies by Technology](actions/search-companies-by-technology.md) | GET | Finds companies in Prospeo by technology. |

### Job Title Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Title Suggestions](actions/get-job-title-suggestions.md) | GET | Finds job title suggestions in Prospeo. |

### Location Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Get Location Suggestions](actions/get-location-suggestions.md) | GET | Finds location suggestions in Prospeo. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Enrich Persons](actions/bulk-enrich-persons.md) | GET | Retrieves enriched person data from Prospeo in bulk. |
| [Bulk Enrich Persons with Mobile](actions/bulk-enrich-persons-with-mobile.md) | GET | Retrieves enriched person data from Prospeo in bulk with mobile numbers. |
| [Enrich Person](actions/enrich-person.md) | GET | Retrieves enriched person data from Prospeo. |
| [Enrich Person by Search Result ID](actions/enrich-person-by-search-result-id.md) | GET | Retrieves enriched person data from Prospeo by search result ID. |
| [Enrich Person with Mobile](actions/enrich-person-with-mobile.md) | GET | Retrieves enriched person data from Prospeo with mobile numbers. |
| [Enrich Person with Verified Email Only](actions/enrich-person-with-verified-email-only.md) | GET | Retrieves enriched person data from Prospeo with verified email only. |
| [Search Persons](actions/search-persons.md) | GET | Finds persons in Prospeo. |
| [Search Persons by Company List](actions/search-persons-by-company-list.md) | GET | Finds persons in Prospeo by company list. |
| [Search Persons by Department](actions/search-persons-by-department.md) | GET | Finds persons in Prospeo by department. |
| [Search Persons by Location](actions/search-persons-by-location.md) | GET | Finds persons in Prospeo by location. |
| [Search Persons by Title and Seniority](actions/search-persons-by-title-and-seniority.md) | GET | Finds persons in Prospeo by title and seniority. |
| [Search Persons with Verified Contact Details](actions/search-persons-with-verified-contact-details.md) | GET | Finds persons in Prospeo with verified contact details. |

