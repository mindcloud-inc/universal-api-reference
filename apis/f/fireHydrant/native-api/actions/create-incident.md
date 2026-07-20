# Create Incident with FireHydrant

Creates a new incident in FireHydrant.

## Endpoint

- **Method:** `POST`
- **Path:** `/incidents`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [Create Incident](https://docs.firehydrant.com/reference/create_incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The incident name. |
| `summary` | body | `string` | no | A short incident summary. |
| `description` | body | `string` | no | Detailed incident description. |
| `severity` | body | `string` | no | The incident severity. |
| `priority` | body | `string` | no | The incident priority. |
| `team_ids` | body | `string<string>` | no | Team IDs to assign to the incident. Send multiple values as a array. |
| `incident_type_id` | body | `string` | no | The incident type ID. |
