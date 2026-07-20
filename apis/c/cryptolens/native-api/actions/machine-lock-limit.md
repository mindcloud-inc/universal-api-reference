# Machine Lock Limit with Cryptolens

Updates a license key machine lock limit in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/key/MachineLockLimit`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Machine Lock Limit](https://app.cryptolens.io/docs/api/v3/MachineLockLimit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
| `NumberOfMachines` | query | `number` | yes | The number of machines allowed. |
