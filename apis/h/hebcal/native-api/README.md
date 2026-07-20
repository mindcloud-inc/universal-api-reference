# Hebcal: Native API Reference

A consolidated summary of Hebcal's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://www.hebcal.com/home/developer-apis
- **API base URL:** `https://www.hebcal.com`

## Authentication

### No authentication

Hebcal public web APIs do not require registration or API keys.

This API does not require request authentication.

[Official authentication documentation](https://www.hebcal.com/home/developer-apis)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Assur Melacha at Date Time](actions/check-assur-melacha-at-date-time.md) | `GET /zmanim` | [docs](https://www.hebcal.com/home/4984/assur-melacha-work-forbidden-api) |
| [Check Assur Melacha Now](actions/check-assur-melacha-now.md) | `GET /zmanim` | [docs](https://www.hebcal.com/home/4984/assur-melacha-work-forbidden-api) |
| [Get Gregorian Date from Hebrew Date](actions/get-gregorian-date-from-hebrew-date.md) | `GET /converter` | [docs](https://www.hebcal.com/home/219/hebrew-date-converter-rest-api) |
| [Get Gregorian Dates for Hebrew Range](actions/get-gregorian-dates-for-hebrew-range.md) | `GET /converter` | [docs](https://www.hebcal.com/home/219/hebrew-date-converter-rest-api) |
| [Get Hebrew Anniversaries](actions/get-hebrew-anniversaries.md) | `POST /yahrzeit` | [docs](https://www.hebcal.com/home/1705/yahrzeit-anniversary-api) |
| [Get Hebrew Birthdays](actions/get-hebrew-birthdays.md) | `POST /yahrzeit` | [docs](https://www.hebcal.com/home/1705/yahrzeit-anniversary-api) |
| [Get Hebrew Date from Gregorian Date](actions/get-hebrew-date-from-gregorian-date.md) | `GET /converter` | [docs](https://www.hebcal.com/home/219/hebrew-date-converter-rest-api) |
| [Get Hebrew Date from Gregorian Parts](actions/get-hebrew-date-from-gregorian-parts.md) | `GET /converter` | [docs](https://www.hebcal.com/home/219/hebrew-date-converter-rest-api) |
| [Get Hebrew Dates for Gregorian Range](actions/get-hebrew-dates-for-gregorian-range.md) | `GET /converter` | [docs](https://www.hebcal.com/home/219/hebrew-date-converter-rest-api) |
| [Get Shabbat Times for Date](actions/get-shabbat-times-for-date.md) | `GET /shabbat` | [docs](https://www.hebcal.com/home/197/shabbat-times-rest-api) |
| [Get Today's Zmanim](actions/get-todays-zmanim.md) | `GET /zmanim` | [docs](https://www.hebcal.com/home/1663/zmanim-halachic-times-api) |
| [Get Torah Reading for Date](actions/get-torah-reading-for-date.md) | `GET /leyning` | [docs](https://www.hebcal.com/home/4277/leyning-torah-reading-api) |
| [Get Torah Readings for Date Range](actions/get-torah-readings-for-date-range.md) | `GET /leyning` | [docs](https://www.hebcal.com/home/4277/leyning-torah-reading-api) |
| [Get Triennial Torah Reading for Date](actions/get-triennial-torah-reading-for-date.md) | `GET /leyning` | [docs](https://www.hebcal.com/home/4277/leyning-torah-reading-api) |
| [Get Weekly Shabbat Times](actions/get-weekly-shabbat-times.md) | `GET /shabbat` | [docs](https://www.hebcal.com/home/197/shabbat-times-rest-api) |
| [Get Yahrzeit Dates](actions/get-yahrzeit-dates.md) | `POST /yahrzeit` | [docs](https://www.hebcal.com/home/1705/yahrzeit-anniversary-api) |
| [Get Yahrzeit Dates with Yizkor](actions/get-yahrzeit-dates-with-yizkor.md) | `POST /yahrzeit` | [docs](https://www.hebcal.com/home/1705/yahrzeit-anniversary-api) |
| [Get Zmanim for Date](actions/get-zmanim-for-date.md) | `GET /zmanim` | [docs](https://www.hebcal.com/home/1663/zmanim-halachic-times-api) |
| [Get Zmanim for Date Range](actions/get-zmanim-for-date-range.md) | `GET /zmanim` | [docs](https://www.hebcal.com/home/1663/zmanim-halachic-times-api) |
| [List Candle-lighting Calendar Events](actions/list-candle-lighting-calendar-events.md) | `GET /hebcal` | [docs](https://www.hebcal.com/home/195/jewish-calendar-rest-api) |
| [List Daf Yomi Readings](actions/list-daf-yomi-readings.md) | `GET /hebcal` | [docs](https://www.hebcal.com/home/195/jewish-calendar-rest-api) |
| [List Jewish Calendar Events](actions/list-jewish-calendar-events.md) | `GET /hebcal` | [docs](https://www.hebcal.com/home/195/jewish-calendar-rest-api) |
| [List Major Holidays](actions/list-major-holidays.md) | `GET /hebcal` | [docs](https://www.hebcal.com/home/195/jewish-calendar-rest-api) |
| [List Minor Holidays](actions/list-minor-holidays.md) | `GET /hebcal` | [docs](https://www.hebcal.com/home/195/jewish-calendar-rest-api) |
| [List Modern Holidays](actions/list-modern-holidays.md) | `GET /hebcal` | [docs](https://www.hebcal.com/home/195/jewish-calendar-rest-api) |
| [List Omer Days](actions/list-omer-days.md) | `GET /hebcal` | [docs](https://www.hebcal.com/home/195/jewish-calendar-rest-api) |
| [List Rosh Chodesh](actions/list-rosh-chodesh.md) | `GET /hebcal` | [docs](https://www.hebcal.com/home/195/jewish-calendar-rest-api) |
| [List Special Shabbatot](actions/list-special-shabbatot.md) | `GET /hebcal` | [docs](https://www.hebcal.com/home/195/jewish-calendar-rest-api) |
| [List Torah Reading Calendar Events](actions/list-torah-reading-calendar-events.md) | `GET /hebcal` | [docs](https://www.hebcal.com/home/195/jewish-calendar-rest-api) |
| [List Yizkor Dates](actions/list-yizkor-dates.md) | `GET /hebcal` | [docs](https://www.hebcal.com/home/195/jewish-calendar-rest-api) |
