# InfluxDB Cloud: List Telegrafs

Retrieves Telegrafs from InfluxDB Cloud.

```
GET https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-telegrafs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InfluxDB Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-telegrafs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-telegrafs?${params}`, {
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
| `limit` | number | no | Maximum number of Telegraf configurations to return. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configurations": [
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
| `configurations` | array<object> |  |

## Native endpoint

Through the native InfluxDB Cloud API, this operation is `GET /telegrafs` (base URL `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-telegrafs.md) for the provider-specific parameters and requirements.

