# Block Key with Cryptolens

Blocks a license key in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/key/BlockKey`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Block Key](https://app.cryptolens.io/docs/api/v3/BlockKey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
