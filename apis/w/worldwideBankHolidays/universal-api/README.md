# <img src="https://images.mindcloud.co/apps/icons/worldwide-bank-holidays_1777583671084.png" alt="Worldwide Bank Holidays logo" width="28" height="28"> Worldwide Bank Holidays: Universal API

Access public holiday, bank holiday, supported country, long weekend, and upcoming holiday data from the Nager.Date public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/worldwideBankHolidays/latest
- **Category:** Productivity / Scheduling
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://date.nager.at
- **Vendor API docs:** https://date.nager.at/API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Today Public Holiday](actions/check-today-public-holiday.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/check-today-public-holiday?connectionId=$CONNECTION_ID&countryCode=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Country

| Action | Method | Description |
| --- | --- | --- |
| [Get Country Info](actions/get-country-info.md) | GET |  |
| [List Available Countries](actions/list-available-countries.md) | GET |  |

### Long Weekend

| Action | Method | Description |
| --- | --- | --- |
| [List Long Weekends](actions/list-long-weekends.md) | GET |  |

### Public Holiday

| Action | Method | Description |
| --- | --- | --- |
| [List Public Holidays](actions/list-public-holidays.md) | GET |  |
| [List Upcoming Public Holidays](actions/list-upcoming-public-holidays.md) | GET |  |
| [List Worldwide Upcoming Public Holidays](actions/list-worldwide-upcoming-public-holidays.md) | GET |  |

### Public Holiday Status

| Action | Method | Description |
| --- | --- | --- |
| [Check Today Public Holiday](actions/check-today-public-holiday.md) | GET |  |

### Version Info

| Action | Method | Description |
| --- | --- | --- |
| [Get API Version](actions/get-api-version.md) | GET |  |

