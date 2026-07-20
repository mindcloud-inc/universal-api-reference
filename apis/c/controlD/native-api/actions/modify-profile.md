# Modify Profile with Control D

Updates a profile in Control D.

## Endpoint

- **Method:** `PUT`
- **Path:** `/profiles/:profileId`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Modify Profile](https://docs.controld.com/reference/put_profiles-profile-id)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | path | `string` | yes | Primary key (PK) of the profile |
| `name` | body | `string` | no | Rename profile to this name |
| `disable_ttl` | body | `number` | no | Disable profile until specified unix timestamp. ttl = 0 disables previous deactivation. |
| `lock_status` | body | `number` | no | Lock/unlock a profile from being edited. |
| `lock_message` | body | `string` | no | Optional message to error our with when locked profile is modified |
| `password` | body | `string` | no | Account password when unlocking a profile |
