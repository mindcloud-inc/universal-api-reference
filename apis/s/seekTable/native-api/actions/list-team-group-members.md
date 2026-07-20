# List Team Group Members with SeekTable

Retrieves members from a SeekTable team group.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/account/:id/team/group/:group_id/member`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [List Team Group Members](https://www.seektable.com/help/self-hosted-admin-accounts-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the user account that owns the team. |
| `group_id` | path | `string` | yes | ID of the team group. |
