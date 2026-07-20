# Update Estimate with MoneyBird

Updates an existing estimate in MoneyBird.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:administrationId/estimates/:estimateId.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Update Estimate](https://developer.moneybird.com/api/estimates/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `estimateId` | path | `string` | yes | Moneybird estimate ID. |
