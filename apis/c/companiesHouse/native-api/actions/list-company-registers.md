# List Company Registers with Companies House

Retrieves company registers from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/registers`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [List Company Registers](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/registers/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
