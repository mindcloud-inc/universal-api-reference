# List Company PSCs with Companies House

Retrieves company persons with significant control from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/persons-with-significant-control`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [List Company PSCs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
| `items_per_page` | query | `string` | yes | The number of PSC records to return per page. |
| `register_view` | query | `string` | yes | Whether to return the register view of the PSC data. |
| `start_index` | query | `string` | yes | The zero-based index of the first PSC record to return. |
