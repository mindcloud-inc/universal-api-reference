# Get Restrictions with Channex

Retrieves rate plan restrictions from Channex.

## Endpoint

- **Method:** `GET`
- **Path:** `/restrictions`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Get Restrictions](https://docs.channex.io/api-v.1-documentation/ari#get-availability-or-restrictions-per-rate-plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[property_id]` | query | `string` | yes | Property UUID used to scope the restrictions query. |
| `filter[date][gte]` | query | `date` | yes | Start date in YYYY-MM-DD format. |
| `filter[date][lte]` | query | `date` | yes | End date in YYYY-MM-DD format. |
| `filter[restrictions]` | query | `string` | no | Restriction selector such as rate, stop_sell, min_stay_arrival, or max_stay. |
