# Remove Organization Member with Zeplin

Removes a member from a Zeplin organization.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organizations/{organization_id}/members/{member_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Remove Organization Member](https://docs.zeplin.dev/reference/removeorganizationmember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | Organization id |
| `member_id` | path | `string` | yes | Member id |
