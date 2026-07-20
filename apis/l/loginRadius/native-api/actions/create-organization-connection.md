# Create Organization Connection with LoginRadius

Creates a new organization connection in LoginRadius.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/manage/organizations/:orgId/connections`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Create Organization Connection](https://www.loginradius.com/docs/api/openapi/create-organization-connection/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Connection domain. |
| `name` | body | `string` | yes | Connection display name. |
| `orgId` | path | `string` | yes | Organization ID that will own the connection. |
