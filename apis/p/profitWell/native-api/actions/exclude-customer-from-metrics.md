# Exclude Customer From Metrics with ProfitWell

Excludes a customer from ProfitWell metrics.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/metrics/exclude_customer/:customer_id/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Exclude Customer From Metrics](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The ID of the customer to exclude. |
