# Remove Feature with Cryptolens

Deletes a feature from a license key in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/key/RemoveFeature`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Remove Feature](https://app.cryptolens.io/docs/api/v3/RemoveFeature)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
| `Feature` | query | `number` | yes | The feature number, 1 to 8 inclusive, that should be removed. |
