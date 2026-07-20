# Calculate Working Day: Native API Reference

A consolidated summary of Calculate Working Day's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-gb/connectors/calculateworkingday/
- **API base URL:** `https://api.mightora.io/calculate-working-day`

## Authentication

### No authentication

The Calculate Working Day connector documentation states no API key is required for use.

This API does not require request authentication.

[Official authentication documentation](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Basic Next Working Day](actions/basic-next-working-day.md) | `GET /basicNextWorkingDay/` | [docs](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#basic-next-working-day) |
| [Combination Of All Calculate Working Day Endpoints](actions/combined.md) | `GET /combined/` | [docs](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#combination-of-all-calculate-working-day-endpoints) |
| [Date Difference Calculator](actions/date-difference-calculator.md) | `GET /dateDifferenceCalculator/` | [docs](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#date-difference-calculator) |
| [Date In X Working Days](actions/date-in-x-working-days.md) | `GET /dateInXWorkingDays/` | [docs](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#date-in-x-working-days) |
| [First And Last Working Day Of Month](actions/first-and-last-working-day-of-month.md) | `GET /firstAndLastWorkingDayOfMonth/` | [docs](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#first-and-last-working-day-of-month) |
| [Is Today A Working Day](actions/is-today-a-working-day.md) | `GET /isTodayAWorkingDay/` | [docs](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#is-today-a-working-day) |
| [Next Working Day](actions/next-working-day.md) | `GET /nextWorkingDay/` | [docs](https://learn.microsoft.com/en-gb/connectors/calculateworkingday/#next-working-day) |
