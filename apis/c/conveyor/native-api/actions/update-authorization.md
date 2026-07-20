# Update Authorization with Conveyor

Updates or revokes an authorization in Conveyor.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/exchange/authorizations/:authorization_id`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [Update Authorization](https://docs.conveyor.com/reference/patch-authorization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authorization_id` | path | `string` | yes | Authorization identifier. |
| `status` | query | `string` | no | Authorization status; Conveyor documents revocation with `revoked`. |
| `access_group_ids[]` | query | `array<string>` | no | Access group identifiers. |
