# Update Organizational Unit with Google Workspace Admin

Updates an organizational unit in Google Workspace Admin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/directory/v1/customer/:customerId/orgunits/:orgUnitPath`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Update Organizational Unit](https://developers.google.com/workspace/admin/directory/reference/rest/v1/orgunits/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Workspace customer identifier. Use my_customer for the current tenant. |
| `description` | body | `string` | no | Updated description for the organizational unit. |
| `name` | body | `string` | no | Updated name for the organizational unit. |
| `orgUnitPath` | path | `string` | yes | Full org unit path without the leading slash, or the org unit ID. |
| `parentOrgUnitPath` | body | `string` | no | Updated parent organizational unit path. |
