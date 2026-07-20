# <img src="https://images.mindcloud.co/apps/icons/cropped-university_1777489698315.png" alt="COVID-19 JHU CSSE logo" width="28" height="28"> COVID-19 JHU CSSE: Universal API

Historical public COVID-19 case, death, recovery, daily report, location lookup, and correction data from the Johns Hopkins University Center for Systems Science and Engineering GitHub repository. JHU CSSE ceased collecting and reporting this dataset on March 10, 2023, so actions return archived historical data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cOVID19JHUCSSE/latest
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://systems.jhu.edu/research/public-health/ncov/
- **Vendor API docs:** https://github.com/CSSEGISandData/COVID-19

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Latest Global Daily Report](actions/list-latest-global-daily-report.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-latest-global-daily-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Covid-19 Location Lookup Rows

| Action | Method | Description |
| --- | --- | --- |
| [List Location Lookup Table](actions/list-location-lookup-table.md) | GET | Retrieves the COVID-19 location lookup rows. |

### Covid-19 Time Series Errata Rows

| Action | Method | Description |
| --- | --- | --- |
| [List Time Series Errata](actions/list-time-series-errata.md) | GET | Retrieves COVID-19 time series errata rows. |

### Global Confirmed Covid-19 Time Series Rows

| Action | Method | Description |
| --- | --- | --- |
| [List Global Confirmed Time Series](actions/list-global-confirmed-time-series.md) | GET | Retrieves global confirmed COVID-19 time series rows. |

### Global Covid-19 Daily Report Rows For A Selected Date

| Action | Method | Description |
| --- | --- | --- |
| [Get Global Daily Report by Date](actions/get-global-daily-report-by-date.md) | GET | Retrieves global COVID-19 daily report rows for a selected date. |

### Global Covid-19 Death Time Series Rows

| Action | Method | Description |
| --- | --- | --- |
| [List Global Deaths Time Series](actions/list-global-deaths-time-series.md) | GET | Retrieves global COVID-19 death time series rows. |

### Global Recovered Covid-19 Time Series Rows

| Action | Method | Description |
| --- | --- | --- |
| [List Global Recovered Time Series](actions/list-global-recovered-time-series.md) | GET | Retrieves global recovered COVID-19 time series rows. |

### Latest Archived Global Covid-19 Daily Report Rows

| Action | Method | Description |
| --- | --- | --- |
| [List Latest Global Daily Report](actions/list-latest-global-daily-report.md) | GET | Retrieves the latest archived global COVID-19 daily report rows. |

### Latest Archived United States Covid-19 Daily Report Rows

| Action | Method | Description |
| --- | --- | --- |
| [List Latest US Daily Report](actions/list-latest-us-daily-report.md) | GET | Retrieves the latest archived United States COVID-19 daily report rows. |

### United States Confirmed Covid-19 Time Series Rows

| Action | Method | Description |
| --- | --- | --- |
| [List US Confirmed Time Series](actions/list-us-confirmed-time-series.md) | GET | Retrieves United States confirmed COVID-19 time series rows. |

### United States Covid-19 Daily Report Rows For A Selected Date

| Action | Method | Description |
| --- | --- | --- |
| [Get US Daily Report by Date](actions/get-us-daily-report-by-date.md) | GET | Retrieves United States COVID-19 daily report rows for a selected date. |

### United States Covid-19 Death Time Series Rows

| Action | Method | Description |
| --- | --- | --- |
| [List US Deaths Time Series](actions/list-us-deaths-time-series.md) | GET | Retrieves United States COVID-19 death time series rows. |

