# Delete Rate Plan with Channex

Deletes a rate plan from Channex.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rate_plans/:id`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Delete Rate Plan](https://docs.channex.io/api-v.1-documentation/rate-plans-collection#remove-rate-plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the rate plan to delete. |
| `force` | query | `boolean` | no | Set true to force removal when supported by Channex. |
