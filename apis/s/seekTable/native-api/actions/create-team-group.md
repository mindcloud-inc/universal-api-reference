# Create Team Group with SeekTable

Creates a new team group in SeekTable.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/account/:id/team/group`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [Create Team Group](https://www.seektable.com/help/self-hosted-admin-accounts-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the user account that owns the team. |
| `Name` | body | `string` | yes | Name of the new team group. |
| `ReportOverrideParameters` | body | `object` | no | Optional key-value map of report parameter overrides for this team group. |
