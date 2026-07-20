# List Activity Categories with ServiceTitan

Retrieves activity categories from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `timesheets/v2/tenant/{tenant}/activity-categories`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Activity Categories](https://developer.servicetitan.io/api-details/#api=tenant-timesheets-v2&operation=ActivityTypes_GetList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `list` | no | What kind of items should be returned (only active items will be returned by default) Values: [True, Any, False] |
| `pageSize` | query | `number` | no | How many records to return (50 by default) |
