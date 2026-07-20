# First And Last Working Day Of Month with Calculate Working Day

Retrieves a month's first and last working days.

## Endpoint

- **Method:** `GET`
- **Path:** `/firstAndLastWorkingDayOfMonth/`
- **Base URL:** `https://api.mightora.io/calculate-working-day`
- **Official documentation:** [First And Last Working Day Of Month](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#first-and-last-working-day-of-month)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | yes | Input date in YYYY-MM-DD format. |
| `working_days` | query | `string` | yes | Comma-separated weekday numbers where Monday is 1. Default is 1,2,3,4,5. |
