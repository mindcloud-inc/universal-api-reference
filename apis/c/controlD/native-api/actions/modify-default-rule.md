# Modify Default Rule with Control D

Updates the default rule in Control D.

## Endpoint

- **Method:** `PUT`
- **Path:** `/profiles/:profileId/default`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Modify Default Rule](https://docs.controld.com/reference/put_profiles-profile-id-default)

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
| `do` | body | `number` | yes | Rule type. 0 = BLOCK. 1 = BYPASS, 2 = SPOOF, 3 = REDIRECT |
| `via` | body | `string` | no | Spoof/Redirect target. If SPOOF, this can be an IP or hostname. If REDIRECT, this must be a valid proxy identifier. |
| `status` | body | `number` | yes | Status of the rule. |
