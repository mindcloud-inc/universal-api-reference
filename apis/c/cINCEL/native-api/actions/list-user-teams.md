# List User Teams with CINCEL

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user/teams`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [List User Teams](https://api.cincel.digital/v3/oas.yaml?tags=digital-signature,auth,tokens)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | path | `number` | yes | User ID whose teams should be listed. |
| `include_deleted` | query | `boolean` | no | Include deleted teams when true. |
| `name_like` | query | `string` | no | Filter teams by partial name. |
