# Get Company PSC Super Secure Beneficial Owner with Companies House

Retrieves a super secure beneficial owner notification from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/persons-with-significant-control/super-secure-beneficial-owner/:super_secure_id`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [Get Company PSC Super Secure Beneficial Owner](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control/super-secure-beneficial-owner/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
| `super_secure_id` | path | `string` | yes | The super secure beneficial owner ID. |
