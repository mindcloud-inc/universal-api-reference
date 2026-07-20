# Get Requirement Validation Result with Grand Avenue Software

Retrieves a requirement validation result from Grand Avenue Software by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/RequirementValidationResults/:id`
- **Base URL:** `{baseUrl}`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `list<string>` | no | Send multiple values as a string. |
| `$expand` | query | `list<string>` | no | Send multiple values as a string. |
| `id` | path | `string` | yes | — |
