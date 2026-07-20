# Get Time Interval Gateway Analytics with Pinata

Retrieves time-interval gateway analytics from Pinata.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/analytics/gateways/time_series`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Get Time Interval Gateway Analytics](https://docs.pinata.cloud/api-reference/endpoint/ipfs/time-interval-gateway-analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_interval` | query | `string` | yes | Date interval (`day` or `week`). |
| `end_date` | query | `string` | yes | End date in YYYY-MM-DD format. |
| `gateway_domain` | query | `string` | yes | Gateway domain to analyze. |
| `sort_by` | query | `string` | yes | Metric to sort by (`requests` or `bandwidth`). |
| `start_date` | query | `string` | yes | Start date in YYYY-MM-DD format. |
