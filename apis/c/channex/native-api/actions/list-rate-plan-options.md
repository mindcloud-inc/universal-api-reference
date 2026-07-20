# List Rate Plan Options with Channex

Retrieves rate plan options from Channex.

## Endpoint

- **Method:** `GET`
- **Path:** `/rate_plans/options`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [List Rate Plan Options](https://docs.channex.io/api-v.1-documentation/rate-plans-collection#rate-plan-options)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[property_id]` | query | `string` | yes | Property UUID required by the rate plan options endpoint. |
