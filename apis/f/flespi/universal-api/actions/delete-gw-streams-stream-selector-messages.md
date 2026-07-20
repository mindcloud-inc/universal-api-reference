# Flespi: Remove all messages from the stream queue.



```
DELETE https://connect.mindcloud.co/v1/universal/flespi/latest/actions/delete-gw-streams-stream-selector-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flespi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/flespi/latest/actions/delete-gw-streams-stream-selector-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flespi/latest/actions/delete-gw-streams-stream-selector-messages?${params}`, {
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
      "errors": [
        {}
      ],
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
| `errors` | array<object> | Flespi response errors. |
| `id` | number | Resource identifier. |
| `name` | string | Resource name. |
| `result` | array<object> | Flespi response result items. |

## Native endpoint

Through the native Flespi API, this operation is `DELETE /gw/streams/{stream.selector}/messages` (base URL `https://flespi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-gw-streams-stream-selector-messages.md) for the provider-specific parameters and requirements.

