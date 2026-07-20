# Invite Organization Member with Zeplin

Invites a member to a Zeplin organization.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/{organization_id}/members`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Invite Organization Member](https://docs.zeplin.dev/reference/inviteorganizationmember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | Organization id |
| `handle` | body | `string` | yes | Email, username or unique identifier of the user |
| `tags[]` | body | `array<string>` | yes | Tags of the user in the organization |
| `role` | body | `string` | yes | The role of the user in the organization ☝️Note that the Developer role maps to `member` and the Reviewer role maps to `alien` in the API. |
| `restricted` | body | `boolean` | yes | Whether the user's membership is restricted to only the projects that they are member of |
