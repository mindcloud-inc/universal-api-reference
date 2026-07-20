# Get Project with Cinode

Retrieves a project from Cinode.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0.1/companies/:companyId/projects/:id`
- **Base URL:** `https://api.cinode.com`
- **Official documentation:** [Get Project](https://api.cinode.com/docs/index.html#/Project/Project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Cinode company ID. |
| `id` | path | `number` | yes | Project ID. |
