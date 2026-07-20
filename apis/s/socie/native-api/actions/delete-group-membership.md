# Delete Group Membership with Socie

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/groups/:groupIdentifier/memberships/:identifier`
- **Base URL:** `https://api.socie.nl`
- **Official documentation:** [Delete Group Membership](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_deleteGroupMembership_context_groupIdentifier_groupsKey_identifier_key_DELETE)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupIdentifier` | path | `string` | yes | The Socie id or externalId of the group. |
| `identifier` | path | `string` | yes | The Socie id or externalId of the group membership. |
