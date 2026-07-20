# Get Company PSC Individual Beneficial Owner with Companies House

Retrieves an individual beneficial owner notification from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/persons-with-significant-control/individual-beneficial-owner/:psc_id`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [Get Company PSC Individual Beneficial Owner](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control/individual-beneficial-owner/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
| `psc_id` | path | `string` | yes | The PSC ID. |
