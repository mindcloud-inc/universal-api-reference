# List Team Users with CINCEL

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:team/users`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [List Team Users](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | UUID of the team whose users should be listed. |
| `include_deleted` | query | `boolean` | no | Include deleted users when true. |
| `name_like` | query | `string` | no | Filter users by partial name match. |
| `email_like` | query | `string` | no | Filter users by partial email match. |
