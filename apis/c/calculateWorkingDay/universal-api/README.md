# <img src="https://images.mindcloud.co/apps/icons/microsoft_1777495389802.png" alt="Calculate Working Day logo" width="28" height="28"> Calculate Working Day: Universal API

Calculate valid working days, next working days, month boundaries, and working-day offsets using Mightora's free Calculate Working Day API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/calculateWorkingDay/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mightora.io/calculate-working-day/
- **Vendor API docs:** https://learn.microsoft.com/en-gb/connectors/calculateworkingday/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Basic Next Working Day](actions/basic-next-working-day.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/basic-next-working-day?connectionId=$CONNECTION_ID&date=2026-04-29" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Working Day

| Action | Method | Description |
| --- | --- | --- |
| [Basic Next Working Day](actions/basic-next-working-day.md) | GET | Retrieves the next Monday-to-Friday working day. |
| [Combination Of All Calculate Working Day Endpoints](actions/combined.md) | GET | Retrieves combined results from all working-day calculations. |
| [Date Difference Calculator](actions/date-difference-calculator.md) | GET | Retrieves total and working-day counts between two dates. |
| [Date In X Working Days](actions/date-in-x-working-days.md) | GET | Retrieves the date after a working-day offset. |
| [First And Last Working Day Of Month](actions/first-and-last-working-day-of-month.md) | GET | Retrieves a month's first and last working days. |
| [Is Today A Working Day](actions/is-today-a-working-day.md) | GET | Retrieves whether a date is a working day. |
| [Next Working Day](actions/next-working-day.md) | GET | Retrieves the next working day using custom working-day rules. |

