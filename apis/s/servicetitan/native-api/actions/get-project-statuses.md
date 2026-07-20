# Get Project Statuses with ServiceTitan

Retrieves project statuses from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.servicetitan.io/jpm/v2/tenant/{tenant}/project-statuses`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Project Statuses](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=ProjectStatuses_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | query | `string` | no |
