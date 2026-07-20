# Update Daily Budgets Batch with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/daily_budgets`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update Daily Budgets Batch](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dailyBudgets[]` | body | `array<object>` | yes | Daily budget records to update in batch. |
