# List Company PSC Statements with Companies House

Retrieves company persons with significant control statements from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/persons-with-significant-control-statements`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [List Company PSC Statements](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control-statements/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
| `items_per_page` | query | `string` | yes | The number of PSC statements to return per page. |
| `register_view` | query | `string` | yes | Whether to return the register view of the PSC statement data. |
| `start_index` | query | `string` | yes | The zero-based index of the first PSC statement to return. |
