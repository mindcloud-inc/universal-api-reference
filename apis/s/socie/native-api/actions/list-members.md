# List Members with Socie

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/members`
- **Base URL:** `https://api.socie.nl`
- **Official documentation:** [List Members](https://resources.socie.nl/docs/api/resource_Members.html#resource_Members_getMembers_context_sort_skip_limit_GET)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of members to return. |
| `skip` | query | `number` | no | Number of members to skip before returning results. |
| `sort` | query | `string` | no | Sort fields in Socie format, for example lastName:desc or lastName:desc,createdAt:asc. |
