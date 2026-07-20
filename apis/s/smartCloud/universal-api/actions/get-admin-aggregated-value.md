# 2Smart Cloud: Aggregated value for topic



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-admin-aggregated-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-admin-aggregated-value?connectionId=$CONNECTION_ID&topic=string&period=string&aggregator=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topic": "string",
  "period": "string",
  "aggregator": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-admin-aggregated-value?${params}`, {
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
| `topic` | string | yes | Metric topic in broker |
| `period` | string | yes |  |
| `aggregator` | string | yes |  |
| `fromTime` | string | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `toTime` | string | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /admin/aggregated-value` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-admin-aggregated-value.md) for the provider-specific parameters and requirements.

