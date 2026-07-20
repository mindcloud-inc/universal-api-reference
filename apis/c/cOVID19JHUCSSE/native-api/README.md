# COVID-19 JHU CSSE: Native API Reference

A consolidated summary of COVID-19 JHU CSSE's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://github.com/CSSEGISandData/COVID-19
- **API base URL:** `https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data`

## Authentication

### No authentication

The JHU CSSE COVID-19 GitHub dataset is publicly accessible and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://github.com/CSSEGISandData/COVID-19)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `text/csv` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Global Daily Report by Date](actions/get-global-daily-report-by-date.md) | `GET /csse_covid_19_daily_reports/:date.csv` | [docs](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports) |
| [Get US Daily Report by Date](actions/get-us-daily-report-by-date.md) | `GET /csse_covid_19_daily_reports_us/:date.csv` | [docs](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports_us) |
| [List Global Confirmed Time Series](actions/list-global-confirmed-time-series.md) | `GET /csse_covid_19_time_series/time_series_covid19_confirmed_global.csv` | [docs](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series) |
| [List Global Deaths Time Series](actions/list-global-deaths-time-series.md) | `GET /csse_covid_19_time_series/time_series_covid19_deaths_global.csv` | [docs](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series) |
| [List Global Recovered Time Series](actions/list-global-recovered-time-series.md) | `GET /csse_covid_19_time_series/time_series_covid19_recovered_global.csv` | [docs](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series) |
| [List Latest Global Daily Report](actions/list-latest-global-daily-report.md) | `GET /csse_covid_19_daily_reports/03-09-2023.csv` | [docs](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports) |
| [List Latest US Daily Report](actions/list-latest-us-daily-report.md) | `GET /csse_covid_19_daily_reports_us/03-09-2023.csv` | [docs](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports_us) |
| [List Location Lookup Table](actions/list-location-lookup-table.md) | `GET /UID_ISO_FIPS_LookUp_Table.csv` | [docs](https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/UID_ISO_FIPS_LookUp_Table.csv) |
| [List Time Series Errata](actions/list-time-series-errata.md) | `GET /csse_covid_19_time_series/Errata.csv` | [docs](https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/csse_covid_19_time_series/Errata.csv) |
| [List US Confirmed Time Series](actions/list-us-confirmed-time-series.md) | `GET /csse_covid_19_time_series/time_series_covid19_confirmed_US.csv` | [docs](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series) |
| [List US Deaths Time Series](actions/list-us-deaths-time-series.md) | `GET /csse_covid_19_time_series/time_series_covid19_deaths_US.csv` | [docs](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series) |
