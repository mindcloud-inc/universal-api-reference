# Extend License with Cryptolens

Extends a license in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/key/ExtendLicense`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Extend License](https://app.cryptolens.io/docs/api/v3/ExtendLicense)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
