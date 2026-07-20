# Add Group Memberships in Bulk with Socie

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/groups/:groupIdentifier/memberships/_bulk`
- **Base URL:** `https://api.socie.nl`
- **Official documentation:** [Add Group Memberships in Bulk](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_addGroupMemberships_context_groupMembershipsInput_groupIdentifier_groupsKey_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupIdentifier` | path | `string` | yes | The Socie id or externalId of the group. |
