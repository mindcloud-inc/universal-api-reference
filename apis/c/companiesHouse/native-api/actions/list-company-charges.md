# List Company Charges with Companies House

Retrieves company charges from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/charges`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [List Company Charges](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/charges/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
