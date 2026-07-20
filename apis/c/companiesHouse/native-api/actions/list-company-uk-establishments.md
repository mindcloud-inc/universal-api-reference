# List Company UK Establishments with Companies House

Retrieves company UK establishments from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/uk-establishments`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [List Company UK Establishments](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/uk-establishments/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
