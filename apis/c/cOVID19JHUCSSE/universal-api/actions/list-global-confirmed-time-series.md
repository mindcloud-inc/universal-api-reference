# COVID-19 JHU CSSE: List Global Confirmed Time Series

Retrieves global confirmed COVID-19 time series rows.

```
GET https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-global-confirmed-time-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a COVID-19 JHU CSSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-global-confirmed-time-series?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-global-confirmed-time-series?${params}`, {
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
      "countryRegion": "string",
      "dateValues": [
        {}
      ],
      "lat": 1,
      "long": 1,
      "provinceState": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryRegion` | string | Country or region name. |
| `dateValues` | array<object> | Cumulative confirmed-case values by ISO date. |
| `lat` | number | Latitude for the reported location. |
| `long` | number | Longitude for the reported location. |
| `provinceState` | string | Province or state name when provided by the source row. |

## Native endpoint

Through the native COVID-19 JHU CSSE API, this operation is `GET /csse_covid_19_time_series/time_series_covid19_confirmed_global.csv` (base URL `https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-global-confirmed-time-series.md) for the provider-specific parameters and requirements.

