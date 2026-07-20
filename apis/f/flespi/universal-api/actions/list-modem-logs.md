# Flespi: List modem logs



```
GET https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-modem-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flespi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-modem-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-modem-logs?${params}`, {
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
      "event": "string",
      "modem_id": 1,
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
| `event` | string | Log event. |
| `modem_id` | number | Modem ID. |
| `result` | array<object> | Flespi response result items. |
| `timestamp` | date | Log timestamp. |

## Native endpoint

Through the native Flespi API, this operation is `GET /gw/modems/all/logs` (base URL `https://flespi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-modem-logs.md) for the provider-specific parameters and requirements.

