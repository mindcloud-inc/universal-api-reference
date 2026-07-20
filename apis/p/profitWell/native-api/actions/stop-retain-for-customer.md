# Stop Retain For Customer with ProfitWell

Stops Retain interventions for a customer in ProfitWell.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/retain/stop/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Stop Retain For Customer](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | yes | The customer ID. |
| `intervention_types[]` | body | `array<string>` | yes | The interventions to stop for the customer. Accepted values: `reactivation`, `retain`, `term_optimization`. |
| `forever` | body | `boolean` | no | Whether to exclude the customer from the chosen interventions going forward. |
