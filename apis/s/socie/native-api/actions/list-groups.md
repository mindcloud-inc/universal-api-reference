# List Groups with Socie

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/groups`
- **Base URL:** `https://api.socie.nl`
- **Official documentation:** [List Groups](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_getGroups_context_sort_skip_limit_GET)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of groups to return. |
| `skip` | query | `number` | no | Number of groups to skip before returning results. |
| `sort` | query | `string` | no | Sort fields in Socie format, for example name:asc. |
