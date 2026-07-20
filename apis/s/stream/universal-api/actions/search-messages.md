# Stream: Search Messages

Finds messages in Stream by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/stream/latest/actions/search-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stream/latest/actions/search-messages?connectionId=$CONNECTION_ID&payload=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "payload": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stream/latest/actions/search-messages?${params}`, {
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
| `payload` | string | yes | JSON-encoded search payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": "string",
      "results": [
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
| `duration` | string |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Stream API, this operation is `GET /search` (base URL `https://chat.stream-io-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-messages.md) for the provider-specific parameters and requirements.

