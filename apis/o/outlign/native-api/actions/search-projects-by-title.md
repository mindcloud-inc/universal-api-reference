# Search Projects By Title with Outlign

Finds projects in Outlign by title.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://go.outlign.co/api/v1`
- **Official documentation:** [Search Projects By Title](https://go.outlign.co/api/docs/projects)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | yes | Filter projects by title using partial match |
| `per_page` | query | `number` | no | Number of results per page (max 1000) |
