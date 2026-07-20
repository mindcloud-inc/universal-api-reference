# Datadog: Query Timeseries Points

Retrieves timeseries points from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/query-timeseries-points
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/query-timeseries-points?connectionId=$CONNECTION_ID&from=1&to=1&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "1",
  "to": "1",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/query-timeseries-points?${params}`, {
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
| `from` | number | yes | Start of the queried time period in epoch seconds. |
| `to` | number | yes | End of the queried time period in epoch seconds. |
| `query` | string | yes | Metrics query string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "from_date": 1,
      "group_by": [
        "string"
      ],
      "message": "string",
      "query": "string",
      "res_type": "string",
      "resp_version": 1,
      "series": [
        {}
      ],
      "status": "string",
      "times": [
        1
      ],
      "to_date": 1,
      "values": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from_date` | number | Start timestamp returned by the query response. |
| `group_by` | array<string> | Grouping dimensions used by the query. |
| `message` | string | Provider response message. |
| `query` | string | Query that was executed. |
| `res_type` | string | Result type returned by Datadog. |
| `resp_version` | number | Response format version. |
| `series` | array<object> | Series returned by the query. |
| `status` | string | Status of the query response. |
| `times` | array<number> | Returned timestamps. |
| `to_date` | number | End timestamp returned by the query response. |
| `values` | array<number> | Returned aggregated values. |

## Native endpoint

Through the native Datadog API, this operation is `GET /api/v1/query` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-timeseries-points.md) for the provider-specific parameters and requirements.

