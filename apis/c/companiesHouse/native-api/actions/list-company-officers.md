# List Company Officers with Companies House

Retrieves company officers from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/officers`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [List Company Officers](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/officers/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
