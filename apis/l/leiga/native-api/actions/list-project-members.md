# List Project Members with Leiga

Retrieves project members from Leiga with pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/project-user-page`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [List Project Members](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741826.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | query | `number` | yes | Project ID |
| `keyword` | query | `string` | no | Keyword for search |
| `pageNumber` | query | `number` | no | Page Number |
| `pageSize` | query | `number` | no | Page Size |
