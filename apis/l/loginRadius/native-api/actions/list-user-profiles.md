# List User Profiles with LoginRadius

Retrieves user profiles from LoginRadius by page.

## Endpoint

- **Method:** `GET`
- **Path:** `https://cloud-api.loginradius.com/identity`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [List User Profiles](https://www.loginradius.com/docs/api/openapi/get-user-profiles-by-page-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `next` | query | `string` | no | Pagination token returned by the previous page. |
| `region` | query | `string` | no | Region filter for the results. |
