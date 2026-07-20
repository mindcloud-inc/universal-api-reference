# 2Smart Cloud: List timelines number



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-timelines-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-timelines-number?connectionId=$CONNECTION_ID&topic=string&period=string&interval=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topic": "string",
  "period": "string",
  "interval": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-timelines-number?${params}`, {
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
      "time": "2026-05-07T12:00:00.000Z",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `time` | date | Timeline timestamp |
| `value` | number | Timeline value |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /vendor/timelines/number` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor-timelines-number.md) for the provider-specific parameters and requirements.

