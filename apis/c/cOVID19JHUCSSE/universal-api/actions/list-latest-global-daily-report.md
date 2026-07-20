# COVID-19 JHU CSSE: List Latest Global Daily Report

Retrieves the latest archived global COVID-19 daily report rows.

```
GET https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-latest-global-daily-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a COVID-19 JHU CSSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-latest-global-daily-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-latest-global-daily-report?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native COVID-19 JHU CSSE API, this operation is `GET /csse_covid_19_daily_reports/03-09-2023.csv` (base URL `https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-latest-global-daily-report.md) for the provider-specific parameters and requirements.

