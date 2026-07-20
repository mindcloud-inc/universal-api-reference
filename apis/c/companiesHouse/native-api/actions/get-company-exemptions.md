# Get Company Exemptions with Companies House

Retrieves company exemptions from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/exemptions`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [Get Company Exemptions](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/exemptions/company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
