# List Client Groups with Nagaris

Finds client groups in Nagaris by filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/client-groups/`
- **Base URL:** `https://core.nagaris.com/api/v1`
- **Official documentation:** [List Client Groups](https://core.nagaris.com/api/v1/schema/redoc/#tag/client-groups/operation/list_client_groups)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search across client group name and code fields. |
| `name` | query | `string` | no | Filter client groups by name contains. |
| `status` | query | `list` | no | Filter by client group status. Accepted values: `0`, `1`, `2`, `3`. |
| `is_finalised` | query | `boolean` | no | Filter by whether the client group is finalised. |
