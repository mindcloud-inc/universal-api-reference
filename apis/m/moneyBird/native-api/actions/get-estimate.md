# Get Estimate with MoneyBird

Retrieves an estimate from MoneyBird.

## Endpoint

- **Method:** `GET`
- **Path:** `/:administrationId/estimates/:estimateId.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Get Estimate](https://developer.moneybird.com/api/estimates/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `estimateId` | path | `string` | yes | Moneybird estimate ID. |
