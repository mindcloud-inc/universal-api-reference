# List Organization Connections with LoginRadius

Retrieves organization connection records from LoginRadius.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/manage/organizations/:orgId/connections`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [List Organization Connections](https://www.loginradius.com/docs/api/openapi/get-all-organization-connections/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Organization ID whose connections should be listed. |
