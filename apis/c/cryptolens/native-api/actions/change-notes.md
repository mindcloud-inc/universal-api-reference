# Change Notes with Cryptolens

Updates notes on a license key in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/key/ChangeNotes`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Change Notes](https://app.cryptolens.io/docs/api/v3/ChangeNotes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
| `Notes` | query | `string` | yes | The notes to save on the license key. |
