# 2Smart Cloud: List timelines string



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-timelines-string
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-timelines-string?connectionId=$CONNECTION_ID&topic=string&period=string&interval=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topic": "string",
  "period": "string",
  "interval": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-timelines-string?${params}`, {
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
| `period` | string | yes | Requested period |
| `interval` | string | yes | Requested interval |
| `limit` | number | no | The number of rows to return |
| `offset` | number | no | Pagination offset |
| `fromTime` | date | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `toTime` | date | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Timeline result rows |
| `meta` | object | Pagination metadata |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /timelines/string` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timelines-string.md) for the provider-specific parameters and requirements.

