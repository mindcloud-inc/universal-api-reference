# Get Company Charge with Companies House

Retrieves a company charge from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/charges/:charge_id`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [Get Company Charge](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/charges/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `charge_id` | path | `string` | yes | The charge ID. |
| `company_number` | path | `string` | yes | The company number. |
