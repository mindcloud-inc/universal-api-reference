# Modify Profile Option with Control D

Updates a profile option in Control D.

## Endpoint

- **Method:** `PUT`
- **Path:** `/profiles/:profileId/options/:name`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Modify Profile Option](https://docs.controld.com/reference/put_profiles-profile-id-options-name)

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
| `name` | path | `string` | yes | Option name |
| `status` | body | `number` | yes | Status of the Profile Option. 1 to enable, 0 to disable |
| `value` | body | `string` | no | Optional value of the option to set |
