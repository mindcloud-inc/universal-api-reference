# Assign Groups For Team Members with SeekTable

Assigns team groups to SeekTable team members.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/account/:id/team/member/assigngroups`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [Assign Groups For Team Members](https://www.seektable.com/help/self-hosted-admin-accounts-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the user account that owns the team. |
| `assignments[]` | body | `array<object>` | yes | Team-member group assignments to apply in one request. |
| `Email` | body | `string` | yes | Login email of the team member to update. |
| `GroupIds[]` | body | `array<string>` | yes | IDs of the team groups that should be assigned to this member. |
