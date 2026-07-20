# List Organizational Units with Google Workspace Admin

Retrieves organizational units from Google Workspace Admin.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/directory/v1/customer/:customerId/orgunits`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [List Organizational Units](https://developers.google.com/workspace/admin/directory/reference/rest/v1/orgunits/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Workspace customer identifier. Use my_customer for the current tenant. |
| `orgUnitPath` | query | `string` | no | Optional parent organizational unit path to list from. |
| `type` | query | `string` | no | Whether to return children only or all nested org units. |
