# List Customer Assigned Users with actiTIME

Retrieves users assigned to a customer in actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/:id/assignedUsers`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Customer Assigned Users](https://www.actitime.com/api-documentation/customers-resource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Customer identifier. |
