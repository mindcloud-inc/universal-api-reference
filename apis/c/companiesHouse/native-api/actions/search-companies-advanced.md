# Search Companies Advanced with Companies House

Finds companies in Companies House by advanced filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/advanced-search/companies`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [Search Companies Advanced](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/search-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name_includes` | query | `string` | no | Filter results to company names containing this text. |
