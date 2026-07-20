# <img src="https://images.mindcloud.co/apps/icons/image-2825-vectorized_1777380608525.png" alt="Zoominfo logo" width="28" height="28"> Zoominfo: Universal API

Search contacts, companies, intent data, and market intelligence

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zoominfo/latest
- **Category:** Marketing
- **Actions:** 84
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zoominfo.com
- **Vendor API docs:** https://api-docs.zoominfo.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (84)

### Authenticate

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | POST | Creates an authentication token in ZoomInfo. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Company](actions/enrich-company.md) | GET | Enriches a company with ZoomInfo data. |
| [Enrich Company Master Data](actions/enrich-company-master-data.md) | GET | Enriches company master data with ZoomInfo data. |
| [Enrich Corporate Hierarchy](actions/enrich-corporate-hierarchy.md) | GET | Enriches a corporate hierarchy with ZoomInfo data. |
| [Enrich Hashtags](actions/enrich-hashtags.md) | GET | Enriches company hashtags with ZoomInfo data. |
| [Enrich Intent](actions/enrich-intent.md) | GET | Enriches company intent data with ZoomInfo data. |
| [Enrich Location](actions/enrich-location.md) | GET | Enriches a location with ZoomInfo data. |
| [Enrich News](actions/enrich-news.md) | GET | Enriches company news with ZoomInfo data. |
| [Enrich Org Chart](actions/enrich-org-chart.md) | GET | Enriches an org chart with ZoomInfo data. |
| [Enrich Scoops](actions/enrich-scoops.md) | GET | Enriches company scoops with ZoomInfo data. |
| [Enrich Technology](actions/enrich-technology.md) | GET | Enriches technology details with ZoomInfo data. |
| [Get Company Ranking](actions/get-company-ranking.md) | GET | Retrieves company ranking values from ZoomInfo. |
| [Get Continents](actions/get-continents.md) | GET | Retrieves continents from ZoomInfo. |
| [Get Countries](actions/get-countries.md) | GET | Retrieves countries from ZoomInfo. |
| [List Companies](actions/list-companies.md) | GET | Finds companies in ZoomInfo by search criteria. |
| [List Intent](actions/list-intent.md) | GET | Finds intent-based companies and contacts in ZoomInfo. |
| [List News](actions/list-news.md) | GET | Finds news in ZoomInfo by search criteria. |
| [List Scoops](actions/list-scoops.md) | GET | Finds scoops in ZoomInfo by search criteria. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Contact](actions/enrich-contact.md) | GET | Enriches a contact with ZoomInfo data. |
| [List Contacts](actions/list-contacts.md) | GET | Finds contacts in ZoomInfo by search criteria. |

### Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Search Inputs](actions/get-company-search-inputs.md) | GET | Retrieves company search input fields from ZoomInfo. |
| [Get Contact Search Inputs](actions/get-contact-search-inputs.md) | GET | Retrieves contact search input fields from ZoomInfo. |
| [Get Usage](actions/get-usage.md) | GET | Retrieves usage details from ZoomInfo. |
| [Lookup Intent Topics](actions/lookup-intent-topics.md) | GET | Retrieves intent topics from ZoomInfo. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Board Members](actions/get-board-members.md) | GET | Retrieves board member values from ZoomInfo. |
| [Get Buying Groups](actions/get-buying-groups.md) | GET | Retrieves buying groups from ZoomInfo. |
| [Get Company Enrich Inputs](actions/get-company-enrich-inputs.md) | GET | Retrieves company enrich input fields from ZoomInfo. |
| [Get Company Enrich Outputs](actions/get-company-enrich-outputs.md) | GET | Retrieves company enrich output fields from ZoomInfo. |
| [Get Company Master Data Enrich Inputs](actions/get-company-master-data-enrich-inputs.md) | GET | Retrieves company master data enrich input fields from ZoomInfo. |
| [Get Company Master Data Enrich Outputs](actions/get-company-master-data-enrich-outputs.md) | GET | Retrieves company master data enrich output fields from ZoomInfo. |
| [Get Company Search Outputs](actions/get-company-search-outputs.md) | GET | Retrieves company search output fields from ZoomInfo. |
| [Get Company Type](actions/get-company-type.md) | GET | Retrieves company types from ZoomInfo. |
| [Get Compliance Inputs](actions/get-compliance-inputs.md) | GET | Retrieves compliance enrich input fields from ZoomInfo. |
| [Get Compliance Outputs](actions/get-compliance-outputs.md) | GET | Retrieves compliance enrich output fields from ZoomInfo. |
| [Get Contact Departments](actions/get-contact-departments.md) | GET | Retrieves contact departments from ZoomInfo. |
| [Get Contact Enrich Inputs](actions/get-contact-enrich-inputs.md) | GET | Retrieves contact enrich input fields from ZoomInfo. |
| [Get Contact Enrich Outputs](actions/get-contact-enrich-outputs.md) | GET | Retrieves contact enrich output fields from ZoomInfo. |
| [Get Contact Search Outputs](actions/get-contact-search-outputs.md) | GET | Retrieves contact search output fields from ZoomInfo. |
| [Get Corporate Hierarchy Enrich Inputs](actions/get-corporate-hierarchy-enrich-inputs.md) | GET | Retrieves corporate hierarchy enrich input fields from ZoomInfo. |
| [Get Corporate Hierarchy Enrich Outputs](actions/get-corporate-hierarchy-enrich-outputs.md) | GET | Retrieves corporate hierarchy enrich output fields from ZoomInfo. |
| [Get Employee Category Band](actions/get-employee-category-band.md) | GET | Retrieves employee category bands from ZoomInfo. |
| [Get Employee Count](actions/get-employee-count.md) | GET | Retrieves employee count ranges from ZoomInfo. |
| [Get Hashtag](actions/get-hashtag.md) | GET | Retrieves hashtag values from ZoomInfo. |
| [Get Hashtag Enrich Inputs](actions/get-hashtag-enrich-inputs.md) | GET | Retrieves hashtag enrich input fields from ZoomInfo. |
| [Get Hierarchy Code](actions/get-hierarchy-code.md) | GET | Retrieves hierarchy codes from ZoomInfo. |
| [Get Industry Codes](actions/get-industry-codes.md) | GET | Retrieves industry codes from ZoomInfo. |
| [Get Intent Enrich Inputs](actions/get-intent-enrich-inputs.md) | GET | Retrieves intent enrich input fields from ZoomInfo. |
| [Get Intent Enrich Outputs](actions/get-intent-enrich-outputs.md) | GET | Retrieves intent enrich output fields from ZoomInfo. |
| [Get Intent Search Inputs](actions/get-intent-search-inputs.md) | GET | Retrieves intent search input fields from ZoomInfo. |
| [Get Intent Search Outputs](actions/get-intent-search-outputs.md) | GET | Retrieves intent search output fields from ZoomInfo. |
| [Get IP Enrich Inputs](actions/get-ip-enrich-inputs.md) | GET | Retrieves IP enrich input fields from ZoomInfo. |
| [Get IP Enrich Outputs](actions/get-ip-enrich-outputs.md) | GET | Retrieves IP enrich output fields from ZoomInfo. |
| [Get Job Function](actions/get-job-function.md) | GET | Retrieves job function values from ZoomInfo. |
| [Get Job Title Hierarchy](actions/get-job-title-hierarchy.md) | GET | Retrieves job title hierarchy values from ZoomInfo. |
| [Get Location Enrich Inputs](actions/get-location-enrich-inputs.md) | GET | Retrieves location enrich input fields from ZoomInfo. |
| [Get Location Enrich Outputs](actions/get-location-enrich-outputs.md) | GET | Retrieves location enrich output fields from ZoomInfo. |
| [Get Management Levels](actions/get-management-levels.md) | GET | Retrieves management levels from ZoomInfo. |
| [Get Metro Area](actions/get-metro-area.md) | GET | Retrieves metro areas from ZoomInfo. |
| [Get NAICS Codes](actions/get-naics-codes.md) | GET | Retrieves NAICS codes from ZoomInfo. |
| [Get News Categories](actions/get-news-categories.md) | GET | Retrieves news categories from ZoomInfo. |
| [Get News Enrich Inputs](actions/get-news-enrich-inputs.md) | GET | Retrieves news enrich input fields from ZoomInfo. |
| [Get News Enrich Outputs](actions/get-news-enrich-outputs.md) | GET | Retrieves news enrich output fields from ZoomInfo. |
| [Get News Search Inputs](actions/get-news-search-inputs.md) | GET | Retrieves news search input fields from ZoomInfo. |
| [Get News Search Outputs](actions/get-news-search-outputs.md) | GET | Retrieves news search output fields from ZoomInfo. |
| [Get Org Chart Enrich Inputs](actions/get-org-chart-enrich-inputs.md) | GET | Retrieves org chart enrich input fields from ZoomInfo. |
| [Get Org Chart Enrich Outputs](actions/get-org-chart-enrich-outputs.md) | GET | Retrieves org chart enrich output fields from ZoomInfo. |
| [Get Revenue Category Band](actions/get-revenue-category-band.md) | GET | Retrieves revenue category bands from ZoomInfo. |
| [Get Revenue Range](actions/get-revenue-range.md) | GET | Retrieves revenue ranges from ZoomInfo. |
| [Get Scoop Departments](actions/get-scoop-departments.md) | GET | Retrieves scoop departments from ZoomInfo. |
| [Get Scoop Enrich Inputs](actions/get-scoop-enrich-inputs.md) | GET | Retrieves scoop enrich input fields from ZoomInfo. |
| [Get Scoop Enrich Outputs](actions/get-scoop-enrich-outputs.md) | GET | Retrieves scoop enrich output fields from ZoomInfo. |
| [Get Scoop Search Inputs](actions/get-scoop-search-inputs.md) | GET | Retrieves scoop search input fields from ZoomInfo. |
| [Get Scoop Search Outputs](actions/get-scoop-search-outputs.md) | GET | Retrieves scoop search output fields from ZoomInfo. |
| [Get Scoop Topics](actions/get-scoop-topics.md) | GET | Retrieves scoop topics from ZoomInfo. |
| [Get Scoop Types](actions/get-scoop-types.md) | GET | Retrieves scoop types from ZoomInfo. |
| [Get SIC Codes](actions/get-sic-codes.md) | GET | Retrieves SIC codes from ZoomInfo. |
| [Get States](actions/get-states.md) | GET | Retrieves states from ZoomInfo. |
| [Get Sub Unit Type](actions/get-sub-unit-type.md) | GET | Retrieves sub-unit types from ZoomInfo. |
| [Get Tech Categories](actions/get-tech-categories.md) | GET | Retrieves tech categories from ZoomInfo. |
| [Get Tech Product](actions/get-tech-product.md) | GET | Retrieves tech product values from ZoomInfo. |
| [Get Tech Skills](actions/get-tech-skills.md) | GET | Retrieves tech skills from ZoomInfo. |
| [Get Tech Vendor](actions/get-tech-vendor.md) | GET | Retrieves tech vendor values from ZoomInfo. |
| [Get Technology Enrich Inputs](actions/get-technology-enrich-inputs.md) | GET | Retrieves technology enrich input fields from ZoomInfo. |
| [Get Years Of Experience](actions/get-years-of-experience.md) | GET | Retrieves years of experience values from ZoomInfo. |

