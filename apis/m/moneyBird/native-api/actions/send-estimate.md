# Send Estimate with MoneyBird

Sends an existing estimate from MoneyBird.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:administrationId/estimates/:estimateId/send_estimate.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Send Estimate](https://developer.moneybird.com/api/estimates/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `estimateId` | path | `string` | yes | Moneybird estimate ID. |
