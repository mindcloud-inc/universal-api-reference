# COVID-19 JHU CSSE: Get US Daily Report by Date

Retrieves United States COVID-19 daily report rows for a selected date.

```
GET https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/get-us-daily-report-by-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a COVID-19 JHU CSSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/get-us-daily-report-by-date?connectionId=$CONNECTION_ID&date=03-09-2023" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "03-09-2023"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/get-us-daily-report-by-date?${params}`, {
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
| `date` | string | yes | Report date in MM-DD-YYYY format. The archived U.S. daily report files are available for dates in the dataset history, with the latest U.S. daily report at 03-09-2023. Default: `03-09-2023`. Example: `03-09-2023`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "caseFatalityRatio": 1,
      "confirmed": 1,
      "countryRegion": "string",
      "deaths": 1,
      "fips": 1,
      "hospitalizationRate": 1,
      "incidentRate": 1,
      "iso3": "string",
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "lat": 1,
      "long": 1,
      "peopleHospitalized": 1,
      "provinceState": "string",
      "recovered": 1,
      "testingRate": 1,
      "totalTestResults": 1,
      "uid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number | Active case count when provided by the source. |
| `caseFatalityRatio` | number | Case fatality ratio reported by the source. |
| `confirmed` | number | Cumulative confirmed cases. |
| `countryRegion` | string | Country or region name. |
| `deaths` | number | Cumulative deaths. |
| `fips` | number | FIPS code when provided. |
| `hospitalizationRate` | number | Hospitalization rate when provided by the source. |
| `incidentRate` | number | Incident rate reported by the source. |
| `iso3` | string | ISO alpha-3 country code. |
| `lastUpdate` | date | Source last update timestamp. |
| `lat` | number | Latitude for the reported location. |
| `long` | number | Longitude for the reported location. |
| `peopleHospitalized` | number | Hospitalization count when provided by the source. |
| `provinceState` | string | U.S. state or territory. |
| `recovered` | number | Recovered count when provided by the source. |
| `testingRate` | number | Testing rate when provided by the source. |
| `totalTestResults` | number | Total test results when provided by the source. |
| `uid` | number | JHU location UID. |

## Native endpoint

Through the native COVID-19 JHU CSSE API, this operation is `GET /csse_covid_19_daily_reports_us/:date.csv` (base URL `https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-us-daily-report-by-date.md) for the provider-specific parameters and requirements.

