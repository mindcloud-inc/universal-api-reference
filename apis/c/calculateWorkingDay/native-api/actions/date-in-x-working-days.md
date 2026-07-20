# Date In X Working Days with Calculate Working Day

Retrieves the date after a working-day offset.

## Endpoint

- **Method:** `GET`
- **Path:** `/dateInXWorkingDays/`
- **Base URL:** `https://api.mightora.io/calculate-working-day`
- **Official documentation:** [Date In X Working Days](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#date-in-x-working-days)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | yes | Input date in YYYY-MM-DD format. |
| `working_days` | query | `string` | yes | Comma-separated weekday numbers where Monday is 1. Default is 1,2,3,4,5. |
| `x_working_days` | query | `number` | yes | Number of working days to look ahead. |
