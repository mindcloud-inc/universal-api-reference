# Get Key with Cryptolens

Retrieves a license key from Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/key/GetKey`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Get Key](https://app.cryptolens.io/docs/api/v3/GetKey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
