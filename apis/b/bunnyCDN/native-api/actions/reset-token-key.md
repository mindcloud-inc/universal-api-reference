# Reset Token Key with BunnyCDN

Resets a BunnyCDN pull zone token key.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:id/resetSecurityKey`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Reset Token Key](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `SecurityKey` | body | `string` | yes | Custom token security key. |
