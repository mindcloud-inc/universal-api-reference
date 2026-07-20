# Show Plan Breakout with Baremetrics

Retrieves metric breakdowns by plan from Baremetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/metrics/:metric/plans`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Show Plan Breakout](https://developers.baremetrics.com/reference/show-plan-breakout)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | — |
| `end_date` | query | `string` | yes | — |
| `metric` | path | `string` | yes | You can see a list of available metrics [here](available-metrics) |
