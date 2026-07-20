# InfluxDB Cloud: List Tasks

Retrieves tasks from InfluxDB Cloud.

```
GET https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InfluxDB Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-tasks?${params}`, {
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
| `limit` | number | no | Maximum number of tasks to return. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": {},
      "tasks": [
        {}
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links` | object |  |
| `tasks` | array<object> |  |
| `totalCount` | number |  |

## Native endpoint

Through the native InfluxDB Cloud API, this operation is `GET /tasks` (base URL `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

