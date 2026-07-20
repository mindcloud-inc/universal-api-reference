# Update Rate Plan with Channex

Updates a rate plan in Channex.

## Endpoint

- **Method:** `PUT`
- **Path:** `/rate_plans/:id`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Update Rate Plan](https://docs.channex.io/api-v.1-documentation/rate-plans-collection#update-rate-plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the rate plan to update. |
| `rate_plan` | body | `object` | yes | Top-level rate_plan payload object documented by Channex for rate plan updates. |
