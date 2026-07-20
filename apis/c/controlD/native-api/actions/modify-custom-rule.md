# Modify Custom Rule with Control D

Updates a custom rule in Control D.

## Endpoint

- **Method:** `PUT`
- **Path:** `/profiles/:profileId/rules`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Modify Custom Rule](https://docs.controld.com/reference/put_profiles-profile-id-rules)

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
| `do` | body | `number` | yes | Rule type. 0 = BLOCK. 1 = BYPASS, 2 = SPOOF, 3 = REDIRECT. |
| `status` | body | `number` | yes | Status of the rule. |
| `via` | body | `string` | no | Spoof/Redirect target. If SPOOF, this can be an IP or hostname. If REDIRECT, this must be a valid proxy identifier. <<glossary:Via>> |
| `via_v6` | body | `string` | no | If SPOOF this can be a valid IPv6 address (AAAA record) |
| `group` | body | `number` | no | ID of the folder to create this rule in. |
| `hostnames[]` | body | `array<string>` | yes | Array of hostnames |
