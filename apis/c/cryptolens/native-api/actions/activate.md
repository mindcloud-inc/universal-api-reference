# Activate with Cryptolens

Activates a license key in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/key/Activate`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Activate](https://app.cryptolens.io/docs/api/v3/Activate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
