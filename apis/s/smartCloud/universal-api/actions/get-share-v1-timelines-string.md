# 2Smart Cloud: List share timelines string



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-share-v1-timelines-string
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-share-v1-timelines-string?connectionId=$CONNECTION_ID&token=string&topic=string&period=string&interval=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "token": "string",
  "topic": "string",
  "period": "string",
  "interval": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-share-v1-timelines-string?${params}`, {
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
| `token` | string | yes | Share token used in request header |
| `topic` | string | yes | Metric topic in broker |
| `period` | string | yes | Requested period |
| `interval` | string | yes | Requested interval |
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Timeline result rows |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /share/v1/timelines/string` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-share-v1-timelines-string.md) for the provider-specific parameters and requirements.

