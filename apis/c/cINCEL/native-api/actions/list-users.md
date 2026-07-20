# List Users with CINCEL

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [List Users](https://docs.cincel.digital/v3/digital-signature#get-/users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_like` | query | `string` | no | Filter users by partial ID match. |
| `name_like` | query | `string` | no | Filter users by partial name match. |
| `email_like` | query | `string` | no | Filter users by partial email match. |
| `role_like` | query | `string` | no | Filter users by the documented role values. |
| `rfc_like` | query | `string` | no | Filter users whose RFC contains this value. |
| `curp_like` | query | `string` | no | Filter users whose CURP contains this value. |
| `job_like` | query | `string` | no | Filter users whose job contains this value. |
