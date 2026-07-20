# List Project Assignments with Productive.io

Retrieves project assignments from your Productive.io account.

## Endpoint

- **Method:** `GET`
- **Path:** `/project_assignments`
- **Base URL:** `https://api.productive.io/api/v2`
- **Official documentation:** [List Project Assignments](https://developer.productive.io/project_assignments.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[person_id]` | query | `string` | no | Filter project assignments by person ID. |
| `filter[project_id]` | query | `string` | no | Filter project assignments by project ID. |
