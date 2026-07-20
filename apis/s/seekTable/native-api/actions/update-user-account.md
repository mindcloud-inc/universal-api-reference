# Update User Account with SeekTable

Updates an existing user account in SeekTable.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/account/:id`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [Update User Account](https://www.seektable.com/help/self-hosted-admin-accounts-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the user account to update. |
| `Email` | body | `string` | no | New login email for the user account. |
| `Name` | body | `string` | no | — |
| `TeamSharing` | body | `boolean` | no | Enable only when the SeekTable installation includes the Team sharing capability. |
| `AdvancedPublishing` | body | `boolean` | no | Enable only when the SeekTable installation includes the Advanced publishing capability. |
