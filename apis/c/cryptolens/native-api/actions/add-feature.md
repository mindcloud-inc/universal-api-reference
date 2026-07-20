# Add Feature with Cryptolens

Adds a feature to a license key in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/key/AddFeature`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Add Feature](https://app.cryptolens.io/docs/api/v3/AddFeature)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
| `Feature` | query | `number` | yes | The feature number, 1 to 8 inclusive, that should be set to true. |
