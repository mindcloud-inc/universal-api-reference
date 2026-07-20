# Update Plan with ProfitWell

Updates a plan in ProfitWell.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/plans/:id/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Update Plan](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the manually-added plan you wish to retrieve or update. |
| `name` | body | `string` | yes | The new name of the plan. |
