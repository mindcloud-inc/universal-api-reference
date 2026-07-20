# 2Smart Cloud: List timelines



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-share-v1-timelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-share-v1-timelines?connectionId=$CONNECTION_ID&topic=string&period=string&interval=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topic": "string",
  "period": "string",
  "interval": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-share-v1-timelines?${params}`, {
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
| `interval` | string | yes |  |
| `fromTime` | string | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `toTime` | string | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
| `data` | array<object> |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /share/v1/timelines` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-share-v1-timelines.md) for the provider-specific parameters and requirements.

