# List Projects with Vercel

Retrieves all project records from Vercel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v10/projects`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [List Projects](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/retrieve-a-list-of-projects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of projects to return |
| `from` | query | `string` | no | Pagination cursor to continue listing projects |
| `search` | query | `string` | no | Search projects by name |
