# Create Plan with ProfitWell

Creates a plan in ProfitWell.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/plans/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Create Plan](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The ID of the new plan. |
| `name` | body | `string` | yes | The name of the plan. |
