# InfluxDB Cloud: Get Query Suggestions

Retrieves query suggestions from InfluxDB Cloud.

```
GET https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/get-query-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InfluxDB Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/get-query-suggestions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/get-query-suggestions?${params}`, {
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
      "funcs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `funcs` | array<object> |  |

## Native endpoint

Through the native InfluxDB Cloud API, this operation is `GET /query/suggestions` (base URL `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-query-suggestions.md) for the provider-specific parameters and requirements.

