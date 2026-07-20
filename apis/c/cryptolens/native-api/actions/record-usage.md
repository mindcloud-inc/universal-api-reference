# Record Usage with Cryptolens

Records subscription usage in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/subscription/RecordUsage`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Record Usage](https://app.cryptolens.io/docs/api/v3/RecordUsage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Key` | query | `string` | yes | The serial key string. |
