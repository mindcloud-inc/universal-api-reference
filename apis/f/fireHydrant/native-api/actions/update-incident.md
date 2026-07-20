# Update Incident with FireHydrant

Updates an existing incident in FireHydrant.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/incidents/:incident_id`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [Update Incident](https://docs.firehydrant.com/reference/update_incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incident_id` | path | `string` | yes | The FireHydrant incident ID. |
| `summary` | body | `string` | no | Update the incident summary. |
| `description` | body | `string` | no | Update the incident description. |
| `severity` | body | `string` | no | Update the incident severity. |
| `priority` | body | `string` | no | Update the incident priority. |
| `incident_type_id` | body | `string` | no | Update the incident type. |
