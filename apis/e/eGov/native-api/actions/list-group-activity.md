# List Group Activity with e-Gov

Retrieves a group's activity stream from e-Gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/group_activity_list`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [List Group Activity](https://data.e-gov.go.jp/data/api/3/action/help_show?name=group_activity_list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | query | `string` | yes |
