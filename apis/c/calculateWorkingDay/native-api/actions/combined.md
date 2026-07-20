# Combination Of All Calculate Working Day Endpoints with Calculate Working Day

Retrieves combined results from all working-day calculations.

## Endpoint

- **Method:** `GET`
- **Path:** `/combined/`
- **Base URL:** `https://api.mightora.io/calculate-working-day`
- **Official documentation:** [Combination Of All Calculate Working Day Endpoints](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#combination-of-all-calculate-working-day-endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | yes | Input date in YYYY-MM-DD format. |
| `working_days` | query | `string` | yes | Comma-separated list of working day numbers where Monday is 1. |
| `x_working_days` | query | `number` | yes | Number of working days to add. |
| `non_working_days` | query | `string` | no | Optional comma-separated dates in YYYY-MM-DD format to treat as non-working days. |
| `country` | query | `list` | no | Optional country value for bank holiday filtering. Accepted values: `0`, `1`, `2`, `3`. |
