# Unblock Key with Cryptolens

Unblocks a license key in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/key/UnblockKey`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Unblock Key](https://app.cryptolens.io/docs/api/v3/UnblockKey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
