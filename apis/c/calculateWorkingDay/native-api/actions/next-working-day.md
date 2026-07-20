# Next Working Day with Calculate Working Day

Retrieves the next working day using custom working-day rules.

## Endpoint

- **Method:** `GET`
- **Path:** `/nextWorkingDay/`
- **Base URL:** `https://api.mightora.io/calculate-working-day`
- **Official documentation:** [Next Working Day](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#next-working-day)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | yes | Input date in YYYY-MM-DD format. |
| `working_days` | query | `string` | yes | Comma-separated weekday numbers where Monday is 1. Default is 1,2,3,4,5. |
| `x_working_days` | query | `number` | yes | Number of working days to look ahead. |
| `non_working_days` | query | `string` | no | Optional comma-separated dates to exclude in YYYY-MM-DD format. |
