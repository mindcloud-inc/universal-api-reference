# COVID-19 JHU CSSE: List Time Series Errata

Retrieves COVID-19 time series errata rows.

```
GET https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-time-series-errata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a COVID-19 JHU CSSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-time-series-errata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-time-series-errata?${params}`, {
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
      "comments": "string",
      "fieldUpdated": "string",
      "file": "string",
      "location": "string",
      "new": 1,
      "old": 1,
      "updateDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string | Source comment or explanation for the correction. |
| `fieldUpdated` | string | Field or date column that was corrected. |
| `file` | string | Source file affected by the correction. |
| `location` | string | Location affected by the correction. |
| `new` | number | Corrected value. |
| `old` | number | Previous value. |
| `updateDate` | date | Date the correction was recorded. |

## Native endpoint

Through the native COVID-19 JHU CSSE API, this operation is `GET /csse_covid_19_time_series/Errata.csv` (base URL `https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-series-errata.md) for the provider-specific parameters and requirements.

