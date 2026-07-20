# Get Project with FreshBooks

Retrieves a project from FreshBooks for a business.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/business/:businessId/project/:projectId`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Get Project](https://www.freshbooks.com/api/project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | path | `string` | yes | FreshBooks business ID. |
| `projectId` | path | `string` | yes | FreshBooks project ID. |
