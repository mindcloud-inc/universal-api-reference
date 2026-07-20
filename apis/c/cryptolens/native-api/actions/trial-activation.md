# Trial Activation with Cryptolens

Enables trial activation on a license in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/key/TrialActivation`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Trial Activation](https://app.cryptolens.io/docs/api/v3/TrialActivation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
| `Enabled` | query | `boolean` | yes | Whether trial activation should be enabled. |
