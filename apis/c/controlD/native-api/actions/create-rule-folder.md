# Create Rule Folder with Control D

Creates a rule folder in Control D.

## Endpoint

- **Method:** `POST`
- **Path:** `/profiles/:profileId/groups`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Create Rule Folder](https://docs.controld.com/reference/post_profiles-profile-id-groups)

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
| `name` | body | `string` | yes | Name of your folder |
| `do` | body | `number` | yes | Add a rule type to a folder. All rules inside will inherit rule type. 0 = BLOCK. 1 = BYPASS, 2 = SPOOF, 3 = REDIRECT |
| `via` | body | `string` | no | Add spoof IP or hostname, or proxy identiifer if do=2 or do=3. |
| `status` | body | `number` | yes | Status of the folder and all rules inside |
