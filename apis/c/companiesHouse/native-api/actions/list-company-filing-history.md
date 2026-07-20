# List Company Filing History with Companies House

Retrieves company filing history from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/filing-history`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [List Company Filing History](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/filing-history/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
