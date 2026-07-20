# Add Group Membership with Socie

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/groups/:groupIdentifier/memberships`
- **Base URL:** `https://api.socie.nl`
- **Official documentation:** [Add Group Membership](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_addGroupMembership_context_groupMembershipInput_groupIdentifier_groupsKey_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupIdentifier` | path | `string` | yes | The Socie id or externalId of the group. |
