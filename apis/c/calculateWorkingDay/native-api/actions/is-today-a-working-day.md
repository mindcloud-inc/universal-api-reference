# Is Today A Working Day with Calculate Working Day

Retrieves whether a date is a working day.

## Endpoint

- **Method:** `GET`
- **Path:** `/isTodayAWorkingDay/`
- **Base URL:** `https://api.mightora.io/calculate-working-day`
- **Official documentation:** [Is Today A Working Day](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#is-today-a-working-day)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | yes | Input date in YYYY-MM-DD format. |
| `working_days` | query | `string` | yes | Comma-separated list of working day numbers where Monday is 1. |
