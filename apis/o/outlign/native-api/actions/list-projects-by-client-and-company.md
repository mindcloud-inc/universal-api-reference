# List Projects by Client and Company with Outlign

Retrieves accessible project records from Outlign.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://go.outlign.co/api/v1`
- **Official documentation:** [List Projects by Client and Company](https://go.outlign.co/api/docs/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `number` | no | Filter projects by company ID. |
| `client_id` | query | `number` | no | Filter projects by client ID. |
