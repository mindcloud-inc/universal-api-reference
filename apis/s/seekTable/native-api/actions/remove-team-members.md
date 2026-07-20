# Remove Team Members with SeekTable

Removes team members from a SeekTable account.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/account/:id/team/member`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [Remove Team Members](https://www.seektable.com/help/self-hosted-admin-accounts-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the user account that owns the team. |
| `emails[]` | body | `array<string>` | yes | Login emails to remove from the owner account's team. |
