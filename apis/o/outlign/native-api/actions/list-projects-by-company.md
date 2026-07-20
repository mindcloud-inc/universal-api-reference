# List Projects By Company with Outlign

Retrieves project records from Outlign by company.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://go.outlign.co/api/v1`
- **Official documentation:** [List Projects By Company](https://go.outlign.co/api/docs/projects)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `number` | yes | Filter projects by company ID |
| `per_page` | query | `number` | no | Number of results per page (max 1000) |
