# Modify Rule Folder with Control D

Updates a rule folder in Control D.

## Endpoint

- **Method:** `PUT`
- **Path:** `/profiles/:profileId/groups/:folder`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Modify Rule Folder](https://docs.controld.com/reference/put_profiles-profile-id-groups-folder)

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
| `folder` | path | `string` | yes | Folder ID |
| `name` | body | `string` | no | Rename the folder to this name |
| `do` | body | `number` | yes | Add a rule type to a folder. All rules inside will inherit rule type |
| `via` | body | `string` | no | Add spoof IP or hostname, or proxy identifer if do=2 or do=3 |
| `status` | body | `number` | yes | Status of the folder and all rules inside |
