# Get Organizational Unit with Google Workspace Admin

Retrieves an organizational unit from Google Workspace Admin.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/directory/v1/customer/:customerId/orgunits/:orgUnitPath`
- **Base URL:** `https://admin.googleapis.com`
- **Official documentation:** [Get Organizational Unit](https://developers.google.com/workspace/admin/directory/reference/rest/v1/orgunits/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Workspace customer identifier. Use my_customer for the current tenant. |
| `orgUnitPath` | path | `string` | yes | Full org unit path without the leading slash, or the org unit ID. |
