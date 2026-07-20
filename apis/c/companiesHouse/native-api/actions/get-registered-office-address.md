# Get Registered Office Address with Companies House

Retrieves a registered office address from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/registered-office-address`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [Get Registered Office Address](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/registered-office-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
