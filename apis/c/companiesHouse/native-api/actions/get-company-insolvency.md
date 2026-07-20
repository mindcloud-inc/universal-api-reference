# Get Company Insolvency with Companies House

Retrieves company insolvency details from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/insolvency`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [Get Company Insolvency](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/insolvency/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
