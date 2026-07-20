# Add Organizational Unit with Google Workspace Admin

Creates an organizational unit in Google Workspace Admin.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/directory/v1/customer/:customerId/orgunits`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Add Organizational Unit](https://developers.google.com/workspace/admin/directory/reference/rest/v1/orgunits/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Workspace customer identifier. Use my_customer for the current tenant. |
| `description` | body | `string` | no | Optional description for the organizational unit. |
| `name` | body | `string` | yes | Name of the new organizational unit. |
| `parentOrgUnitPath` | body | `string` | yes | Parent organizational unit path. |
