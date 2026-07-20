# Bureau of Labor Statistics: Query Series Data

Finds Bureau of Labor Statistics data for one or more series.

```
GET https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/query-series-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bureau of Labor Statistics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/query-series-data?connectionId=$CONNECTION_ID&seriesid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "seriesid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/query-series-data?${params}`, {
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
| `seriesid` | string<string> | yes | One or more BLS series IDs. BLS expects the JSON key seriesid with an array of IDs. Accepts multiple values as an array. |
| `startyear` | string | no | Optional four-digit start year for the requested time frame. |
| `endyear` | string | no | Optional four-digit end year for the requested time frame. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `catalog` | boolean | no | Optional BLS flag to include catalog metadata when available. BLS registration may be required for enhanced optional fields. Default: `false`. |
| `calculations` | boolean | no | Optional BLS flag to include available net and percent calculations. BLS registration may be required for enhanced optional fields. Default: `false`. |
| `annualaverage` | boolean | no | Optional BLS flag to include annual averages when available. BLS registration may be required for enhanced optional fields. Default: `false`. |
| `aspects` | boolean | no | Optional BLS flag to retrieve aspects associated with data points when available. BLS registration may be required for enhanced optional fields. Default: `false`. |

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

Through the native Bureau of Labor Statistics API, this operation is `POST /timeseries/data/` (base URL `https://api.bls.gov/publicAPI/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-series-data.md) for the provider-specific parameters and requirements.

