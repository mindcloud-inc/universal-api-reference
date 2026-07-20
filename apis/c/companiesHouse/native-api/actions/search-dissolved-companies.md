# Search Dissolved Companies with Companies House

Finds dissolved companies in Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/dissolved-search/companies`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [Search Dissolved Companies](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/search-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The search term. |
| `search_type` | query | `string` | yes | The dissolved company search type. |
