# List Group Memberships with Socie

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/groups/:groupIdentifier/memberships`
- **Base URL:** `https://api.socie.nl`
- **Official documentation:** [List Group Memberships](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_getGroupMemberships_context_groupIdentifier_groupsKey_sort_skip_limit_GET)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupIdentifier` | path | `string` | yes | The Socie id or externalId of the group. |
| `limit` | query | `number` | no | Maximum number of memberships to return. |
| `skip` | query | `number` | no | Number of memberships to skip before returning results. |
| `sort` | query | `string` | no | Sort fields in Socie format, for example orderNumber:asc. |
