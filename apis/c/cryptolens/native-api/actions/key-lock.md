# Key Lock with Cryptolens

Locks an access token to a license key in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/auth/KeyLock`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Key Lock](https://app.cryptolens.io/docs/api/v3/KeyLock)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
