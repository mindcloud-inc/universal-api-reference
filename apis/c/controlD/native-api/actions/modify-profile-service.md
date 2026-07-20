# Modify Profile Service with Control D

Updates a profile service in Control D.

## Endpoint

- **Method:** `PUT`
- **Path:** `/profiles/:profileId/services/:service`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Modify Profile Service](https://docs.controld.com/reference/put_profiles-profile-id-services-service)

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
| `service` | path | `string` | yes | Service name |
| `do` | body | `number` | yes | Rule type. 0 = BLOCK. 1 = BYPASS, 2 = SPOOF, 3 = REDIRECT. |
| `status` | body | `number` | yes | Rule status. 0 = disable. 1 = enabled |
| `via` | body | `string` | no | Spoof/Redirect target. If SPOOF, this can be an IPv4 or hostname. If REDIRECT, this must be a valid proxy identifier. <<glossary:Via>> |
| `via_v6` | body | `string` | no | If SPOOF this can be a valid IPv6 address (AAAA record) |
