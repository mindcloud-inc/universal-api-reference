# Get Company PSC Statement with Companies House

Retrieves a person with significant control statement from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/persons-with-significant-control-statements/:statement_id`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [Get Company PSC Statement](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control-statements/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
| `statement_id` | path | `string` | yes | The PSC statement ID. |
