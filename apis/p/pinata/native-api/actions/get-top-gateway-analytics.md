# Get Top Gateway Analytics with Pinata

Retrieves top gateway analytics from Pinata.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/analytics/gateways/top`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Get Top Gateway Analytics](https://docs.pinata.cloud/api-reference/endpoint/ipfs/top-gateway-analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `by` | query | `string` | yes | Aggregation field (`cid`, `country`, `region`, `user_agent`, `referrer`, or `file_name`). |
| `end_date` | query | `string` | yes | End date in YYYY-MM-DD format. |
| `gateway_domain` | query | `string` | yes | Gateway domain to analyze. |
| `sort_by` | query | `string` | yes | Metric to sort by (`requests` or `bandwidth`). |
| `start_date` | query | `string` | yes | Start date in YYYY-MM-DD format. |
