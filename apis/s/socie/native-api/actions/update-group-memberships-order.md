# Update Group Memberships Order with Socie

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/groups/:groupIdentifier/memberships/order`
- **Base URL:** `https://api.socie.nl`
- **Official documentation:** [Update Group Memberships Order](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_updateGroupMembershipsOrder_context_groupIdentifier_groupsKey_orderInput_PATCH)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupIdentifier` | path | `string` | yes | The Socie id or externalId of the group. |
