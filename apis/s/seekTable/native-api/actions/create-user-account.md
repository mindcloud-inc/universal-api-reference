# Create User Account with SeekTable

Creates a new user account in SeekTable.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/account`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [Create User Account](https://www.seektable.com/help/self-hosted-admin-accounts-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | yes | Login email for the new SeekTable account. |
| `Name` | body | `string` | no | — |
| `TeamSharing` | body | `boolean` | no | Enable only when the SeekTable installation includes the Team sharing capability. |
| `AdvancedPublishing` | body | `boolean` | no | Enable only when the SeekTable installation includes the Advanced publishing capability. |
