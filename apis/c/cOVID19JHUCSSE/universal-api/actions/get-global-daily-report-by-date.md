# COVID-19 JHU CSSE: Get Global Daily Report by Date

Retrieves global COVID-19 daily report rows for a selected date.

```
GET https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/get-global-daily-report-by-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a COVID-19 JHU CSSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/get-global-daily-report-by-date?connectionId=$CONNECTION_ID&date=03-09-2023" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "03-09-2023"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/get-global-daily-report-by-date?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | yes | Report date in MM-DD-YYYY format. The archived daily report files are available for dates in the dataset history, with the latest global daily report at 03-09-2023. Default: `03-09-2023`. Example: `03-09-2023`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "admin2": "string",
      "caseFatalityRatio": 1,
      "combinedKey": "string",
      "confirmed": 1,
      "countryRegion": "string",
      "deaths": 1,
      "fips": 1,
      "incidentRate": 1,
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "lat": 1,
      "long": 1,
      "provinceState": "string",
      "recovered": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number | Active case count when provided by the source. |
| `admin2` | string | County or equivalent local administrative area. |
| `caseFatalityRatio` | number | Case fatality ratio reported by the source. |
| `combinedKey` | string | Combined source location label. |
| `confirmed` | number | Cumulative confirmed cases. |
| `countryRegion` | string | Country or region name. |
| `deaths` | number | Cumulative deaths. |
| `fips` | number | FIPS code when provided. |
| `incidentRate` | number | Incident rate reported by the source. |
| `lastUpdate` | date | Source last update timestamp. |
| `lat` | number | Latitude for the reported location. |
| `long` | number | Longitude for the reported location. |
| `provinceState` | string | Province or state name when provided. |
| `recovered` | number | Recovered count when provided by the source. |

## Native endpoint

Through the native COVID-19 JHU CSSE API, this operation is `GET /csse_covid_19_daily_reports/:date.csv` (base URL `https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-global-daily-report-by-date.md) for the provider-specific parameters and requirements.

