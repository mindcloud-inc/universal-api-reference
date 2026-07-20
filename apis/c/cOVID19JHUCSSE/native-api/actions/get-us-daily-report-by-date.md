# Get US Daily Report by Date with COVID-19 JHU CSSE

Retrieves United States COVID-19 daily report rows for a selected date.

## Endpoint

- **Method:** `GET`
- **Path:** `/csse_covid_19_daily_reports_us/:date.csv`
- **Base URL:** `https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data`
- **Official documentation:** [Get US Daily Report by Date](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports_us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | Report date in MM-DD-YYYY format. The archived U.S. daily report files are available for dates in the dataset history, with the latest U.S. daily report at 03-09-2023. |
