# Bureau of Labor Statistics: List Popular Series

Retrieves popular Bureau of Labor Statistics series IDs.

```
GET https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/list-popular-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bureau of Labor Statistics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/list-popular-series?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/list-popular-series?${params}`, {
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
| `survey` | string | no | Optional BLS survey abbreviation, for example LA, to return popular series for one survey. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": [
        "string"
      ],
      "responseTime": 1,
      "Results": {
        "series": [
          {
            "seriesID": "string"
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | array<string> | BLS response messages. |
| `responseTime` | number | BLS response time in milliseconds. |
| `Results` | object | BLS response results envelope. |
| `Results.series` | array<object> | Popular series returned by BLS. |
| `Results.series[].seriesID` | string | BLS series ID. |
| `status` | string | BLS request status returned by runtime. |

## Native endpoint

Through the native Bureau of Labor Statistics API, this operation is `GET /timeseries/popular` (base URL `https://api.bls.gov/publicAPI/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-popular-series.md) for the provider-specific parameters and requirements.

