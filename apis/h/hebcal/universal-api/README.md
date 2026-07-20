# <img src="https://images.mindcloud.co/apps/icons/hebcal_1776045069480.png" alt="Hebcal logo" width="28" height="28"> Hebcal: Universal API

Public Jewish calendar and zmanim API for Hebrew date conversion, holiday calendars, Torah readings, Shabbat times, yahrzeit schedules, and halachic times.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hebcal/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hebcal.com
- **Vendor API docs:** https://www.hebcal.com/home/developer-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Assur Melacha at Date Time](actions/check-assur-melacha-at-date-time.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/check-assur-melacha-at-date-time?connectionId=$CONNECTION_ID&dt=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Hebrew Anniversaries](actions/get-hebrew-anniversaries.md) | GET | Retrieves Hebrew anniversaries from Hebcal. |
| [Get Hebrew Birthdays](actions/get-hebrew-birthdays.md) | GET | Retrieves Hebrew birthdays from Hebcal. |
| [Get Torah Reading for Date](actions/get-torah-reading-for-date.md) | GET | Retrieves the Torah reading for a date from Hebcal. |
| [Get Torah Readings for Date Range](actions/get-torah-readings-for-date-range.md) | GET | Retrieves Torah readings for a date range from Hebcal. |
| [Get Triennial Torah Reading for Date](actions/get-triennial-torah-reading-for-date.md) | GET | Retrieves the triennial Torah reading for a date from Hebcal. |
| [Get Yahrzeit Dates](actions/get-yahrzeit-dates.md) | GET | Retrieves yahrzeit dates from Hebcal. |
| [Get Yahrzeit Dates with Yizkor](actions/get-yahrzeit-dates-with-yizkor.md) | GET | Retrieves yahrzeit dates with Yizkor from Hebcal. |
| [List Candle-lighting Calendar Events](actions/list-candle-lighting-calendar-events.md) | GET | Retrieves candle-lighting calendar events from Hebcal. |
| [List Daf Yomi Readings](actions/list-daf-yomi-readings.md) | GET | Retrieves Daf Yomi readings from Hebcal. |
| [List Jewish Calendar Events](actions/list-jewish-calendar-events.md) | GET | Retrieves Jewish calendar events from Hebcal. |
| [List Major Holidays](actions/list-major-holidays.md) | GET | Retrieves major holidays from Hebcal. |
| [List Minor Holidays](actions/list-minor-holidays.md) | GET | Retrieves minor holidays from Hebcal. |
| [List Modern Holidays](actions/list-modern-holidays.md) | GET | Retrieves modern holidays from Hebcal. |
| [List Omer Days](actions/list-omer-days.md) | GET | Retrieves Omer days from Hebcal. |
| [List Rosh Chodesh](actions/list-rosh-chodesh.md) | GET | Retrieves Rosh Chodesh dates from Hebcal. |
| [List Special Shabbatot](actions/list-special-shabbatot.md) | GET | Retrieves special Shabbatot from Hebcal. |
| [List Torah Reading Calendar Events](actions/list-torah-reading-calendar-events.md) | GET | Retrieves Torah reading calendar events from Hebcal. |
| [List Yizkor Dates](actions/list-yizkor-dates.md) | GET | Retrieves Yizkor dates from Hebcal. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get Shabbat Times for Date](actions/get-shabbat-times-for-date.md) | GET | Retrieves Shabbat times for a date from Hebcal. |
| [Get Today's Zmanim](actions/get-todays-zmanim.md) | GET | Retrieves today's zmanim from Hebcal. |
| [Get Weekly Shabbat Times](actions/get-weekly-shabbat-times.md) | GET | Retrieves weekly Shabbat times from Hebcal. |
| [Get Zmanim for Date](actions/get-zmanim-for-date.md) | GET | Retrieves zmanim for a date from Hebcal. |
| [Get Zmanim for Date Range](actions/get-zmanim-for-date-range.md) | GET | Retrieves zmanim for a date range from Hebcal. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Check Assur Melacha at Date Time](actions/check-assur-melacha-at-date-time.md) | GET | Checks whether work is forbidden at a date and time in Hebcal. |
| [Check Assur Melacha Now](actions/check-assur-melacha-now.md) | GET | Checks whether work is forbidden now in Hebcal. |
| [Get Gregorian Date from Hebrew Date](actions/get-gregorian-date-from-hebrew-date.md) | GET | Retrieves a Gregorian date from a Hebrew date in Hebcal. |
| [Get Gregorian Dates for Hebrew Range](actions/get-gregorian-dates-for-hebrew-range.md) | GET | Retrieves Gregorian dates for a Hebrew date range in Hebcal. |
| [Get Hebrew Date from Gregorian Date](actions/get-hebrew-date-from-gregorian-date.md) | GET | Retrieves a Hebrew date from a Gregorian date in Hebcal. |
| [Get Hebrew Date from Gregorian Parts](actions/get-hebrew-date-from-gregorian-parts.md) | GET | Retrieves a Hebrew date from Gregorian date parts in Hebcal. |
| [Get Hebrew Dates for Gregorian Range](actions/get-hebrew-dates-for-gregorian-range.md) | GET | Retrieves Hebrew dates for a Gregorian date range in Hebcal. |

