# Get Employees with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `settings/v2/tenant/{tenant}/employees`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Employees](https://developer.servicetitan.io/api-details/#api=tenant-settings-v2&operation=Employees_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | query | `boolean` | no |
| `name` | query | `string` | no |
| `ids` | query | `string` | no |
