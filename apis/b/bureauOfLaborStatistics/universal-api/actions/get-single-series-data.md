# Bureau of Labor Statistics: Get Single Series Data

Retrieves recent data for one Bureau of Labor Statistics series.

```
GET https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/get-single-series-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bureau of Labor Statistics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/get-single-series-data?connectionId=$CONNECTION_ID&seriesId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "seriesId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/get-single-series-data?${params}`, {
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
| `seriesId` | string | yes | BLS time series ID. Use uppercase BLS format, for example LAUCN040010000000005. |

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
            "data": [
              {
                "footnotes": [
                  {
                    "code": "string",
                    "text": "string"
                  }
                ],
                "latest": "string",
                "period": "string",
                "periodName": "Ava Chen",
                "value": "string",
                "year": "string"
              }
            ],
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
| `Results.series` | array<object> | Series returned by BLS. |
| `Results.series[].data` | array<object> | Data points for the series. |
| `Results.series[].data[].footnotes` | array<object> | Footnotes for the data point. |
| `Results.series[].data[].footnotes[].code` | string | Optional BLS footnote code. |
| `Results.series[].data[].footnotes[].text` | string | Optional BLS footnote text. |
| `Results.series[].data[].latest` | string | Present when BLS marks the data point as latest. |
| `Results.series[].data[].period` | string | BLS period code. |
| `Results.series[].data[].periodName` | string | Human-readable period name. |
| `Results.series[].data[].value` | string | Data point value as returned by BLS. |
| `Results.series[].data[].year` | string | Data point year. |
| `Results.series[].seriesID` | string | BLS series ID. |
| `status` | string | BLS request status returned by runtime. |

## Native endpoint

Through the native Bureau of Labor Statistics API, this operation is `GET /timeseries/data/:seriesId` (base URL `https://api.bls.gov/publicAPI/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-series-data.md) for the provider-specific parameters and requirements.

