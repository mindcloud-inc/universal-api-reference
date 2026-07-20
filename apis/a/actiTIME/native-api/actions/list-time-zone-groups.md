# List Time Zone Groups with actiTIME

Retrieves time zone groups from actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeZoneGroups`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Time Zone Groups](https://www.actitime.com/api-documentation/time-zone-groups-resource)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Exact time zone group name match, case-insensitive. |
| `sort` | query | `string` | no | Sorting tokens like +name or -name. |
