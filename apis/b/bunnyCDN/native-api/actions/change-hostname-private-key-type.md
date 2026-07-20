# Change Hostname Private Key Type with BunnyCDN

Updates a BunnyCDN hostname private key type.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:id/updatePrivateKeyType`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Change Hostname Private Key Type](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `Hostname` | body | `string` | yes | Hostname whose private key type will be changed. |
| `KeyType` | body | `string` | yes | Certificate private key type enum value. |
