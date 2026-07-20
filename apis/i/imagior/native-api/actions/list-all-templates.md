# List All Templates with Imagior

Retrieves templates from Imagior.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/all`
- **Base URL:** `https://api.imagior.com`
- **Official documentation:** [List All Templates](https://docs.imagior.com/api-reference/retrieve-all-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Sort by `createdAt` or `updatedAt`. Defaults to `updatedAt`. |
| `order` | query | `string` | no | Sort order, either `asc` or `desc`. Defaults to `desc`. |
