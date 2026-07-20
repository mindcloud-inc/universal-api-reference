# Deactivate with Cryptolens

Deactivates a license key in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/key/Deactivate`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Deactivate](https://app.cryptolens.io/docs/api/v3/Deactivate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
