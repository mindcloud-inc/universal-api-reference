# List Workspaces with ContentStudio

Retrieves workspaces for the authenticated user from ContentStudio.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces`
- **Base URL:** `https://api.contentstudio.io/api/v1`
- **Official documentation:** [List Workspaces](https://api-prod.contentstudio.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for pagination. |
| `per_page` | query | `number` | no | Number of items per page. |
