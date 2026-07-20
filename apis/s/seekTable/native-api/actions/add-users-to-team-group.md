# Add Users To Team Group with SeekTable

Adds users to a SeekTable team group.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/account/:id/team/group/:group_id/member`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [Add Users To Team Group](https://www.seektable.com/help/self-hosted-admin-accounts-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the user account that owns the team. |
| `group_id` | path | `string` | yes | ID of the team group. |
| `emails[]` | body | `array<string>` | yes | Login emails to add to the specified team group. |
