# Update Daily Revenue Batch with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/daily_revenue`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update Daily Revenue Batch](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dailyRevenue[]` | body | `array<object>` | yes | Daily revenue records to update in batch. |
