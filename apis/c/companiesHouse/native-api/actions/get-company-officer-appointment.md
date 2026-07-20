# Get Company Officer Appointment with Companies House

Retrieves a company officer appointment from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/appointments/:appointment_id`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [Get Company Officer Appointment](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/officers/appointment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appointment_id` | path | `string` | yes | The appointment ID. |
| `company_number` | path | `string` | yes | The company number. |
