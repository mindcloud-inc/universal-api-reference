# Flespi: List streams



```
GET https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-streams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flespi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-streams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-streams?${params}`, {
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
      "enabled": true,
      "id": 1,
      "name": "Ava Chen",
      "result": [
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
| `enabled` | boolean | Whether the stream is enabled. |
| `id` | number | Stream ID. |
| `name` | string | Stream name. |
| `result` | array<object> | Flespi response result items. |

## Native endpoint

Through the native Flespi API, this operation is `GET /gw/streams/all` (base URL `https://flespi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-streams.md) for the provider-specific parameters and requirements.

