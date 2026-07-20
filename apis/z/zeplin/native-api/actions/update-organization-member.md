# Update Organization Member with Zeplin

Updates an existing organization member in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/organizations/{organization_id}/members/{member_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Organization Member](https://docs.zeplin.dev/reference/updateorganizationmember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | Organization id |
| `member_id` | path | `string` | yes | Member id |
| `tags[]` | body | `array<string>` | yes | Tags of the user in the organization |
| `role` | body | `string` | yes | The role of the user in the organization ☝️Note that the Developer role maps to `member` and the Reviewer role maps to `alien` in the API. |
| `restricted` | body | `boolean` | yes | Whether the user's membership is restricted to only the |
