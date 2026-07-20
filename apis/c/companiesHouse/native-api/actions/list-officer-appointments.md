# List Officer Appointments with Companies House

Retrieves officer appointments from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/officers/:officer_id/appointments`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [List Officer Appointments](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/officers/appointments/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `officer_id` | path | `string` | yes | The officer ID. |
