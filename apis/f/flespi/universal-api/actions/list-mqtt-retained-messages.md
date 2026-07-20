# Flespi: List MQTT retained messages



```
GET https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-mqtt-retained-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flespi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-mqtt-retained-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-mqtt-retained-messages?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "payload": "string",
      "result": [
        {}
      ],
      "topic": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Created timestamp. |
| `payload` | string | Retained payload. |
| `result` | array<object> | Flespi response result items. |
| `topic` | string | MQTT topic. |

## Native endpoint

Through the native Flespi API, this operation is `GET /mqtt/messages/all` (base URL `https://flespi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mqtt-retained-messages.md) for the provider-specific parameters and requirements.

