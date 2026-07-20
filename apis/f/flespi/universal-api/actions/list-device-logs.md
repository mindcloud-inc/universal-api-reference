# Flespi: List device logs



```
GET https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-device-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flespi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-device-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-device-logs?${params}`, {
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
      "device_id": 1,
      "event": "string",
      "result": [
        {}
      ],
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `device_id` | number | Device ID. |
| `event` | string | Log event. |
| `result` | array<object> | Flespi response result items. |
| `timestamp` | date | Log timestamp. |

## Native endpoint

Through the native Flespi API, this operation is `GET /gw/devices/all/logs` (base URL `https://flespi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-device-logs.md) for the provider-specific parameters and requirements.

