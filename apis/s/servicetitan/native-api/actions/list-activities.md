# List Activities with ServiceTitan

Retrieves activities from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `timesheets/v2/tenant/{tenant}/activities`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Activities](https://developer.servicetitan.io/api-details/#api=tenant-timesheets-v2&operation=ActivitiesControllers_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeTotal` | query | `boolean` | no | Whether total count should be returned Format: `toggle`. |
| `createdBefore` | query | `string` | no | Return items created before certain date/time (in UTC) |
| `createdOnOrAfter` | query | `string` | no | Return items created on or after certain date/time (in UTC) |
| `modifiedBefore` | query | `string` | no | Return items modified before certain date/time (in UTC) |
| `modifiedOnOrAfter` | query | `string` | no | Return items modified on or after certain date/time (in UTC) |
| `active` | query | `list` | no | What kind of items should be returned (only active items will be returned by default) Values: [True, Any, False] |
| `sort` | query | `string` | no | Applies sorting by specified fields |
