# Get Company Profile with Companies House

Retrieves a company profile from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [Get Company Profile](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/company-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
