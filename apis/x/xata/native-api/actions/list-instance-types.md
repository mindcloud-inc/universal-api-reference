# Get available instance types with Xata

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationID/instanceTypes`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Get available instance types](https://xata.io/docs/api-reference/projects/get-available-instance-types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization to check instance type availability for |
| `region` | query | `string` | yes | Region to check instance type availability for |
