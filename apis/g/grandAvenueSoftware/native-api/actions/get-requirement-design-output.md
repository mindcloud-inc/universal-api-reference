# Get Requirement Design Output with Grand Avenue Software

Retrieves a requirement design output from Grand Avenue Software by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/RequirementDesignOutputs/:id`
- **Base URL:** `{baseUrl}`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `list<string>` | no | Send multiple values as a string. |
| `$expand` | query | `list<string>` | no | Send multiple values as a string. |
| `id` | path | `string` | yes | — |
