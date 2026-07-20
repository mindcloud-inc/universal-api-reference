# Export Users with Flexopus

Retrieves a user export from Flexopus.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/export`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [Export Users](https://flexopus.com/api/docs/#endpoints-GETapi-v1-users-export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | query | `string` | yes | The export file format. |
