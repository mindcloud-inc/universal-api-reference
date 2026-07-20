# Date Difference Calculator with Calculate Working Day

Retrieves total and working-day counts between two dates.

## Endpoint

- **Method:** `GET`
- **Path:** `/dateDifferenceCalculator/`
- **Base URL:** `https://api.mightora.io/calculate-working-day`
- **Official documentation:** [Date Difference Calculator](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#date-difference-calculator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `date` | yes | Start date in YYYY-MM-DD format. |
| `end_date` | query | `date` | yes | End date in YYYY-MM-DD format. |
| `working_days` | query | `string` | yes | Comma-separated list of working day numbers where Monday is 1. |
| `non_working_days` | query | `string` | no | Optional comma-separated dates in YYYY-MM-DD format to treat as non-working days. |
