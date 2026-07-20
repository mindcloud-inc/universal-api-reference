# Update Group Membership with Socie

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/groups/:groupIdentifier/memberships/:identifier`
- **Base URL:** `https://api.socie.nl`
- **Official documentation:** [Update Group Membership](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_updateGroupMembership_context_groupIdentifier_groupsKey_identifier_key_patchInput_PATCH)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupIdentifier` | path | `string` | yes | The Socie id or externalId of the group. |
| `identifier` | path | `string` | yes | The Socie id or externalId of the group membership. |
