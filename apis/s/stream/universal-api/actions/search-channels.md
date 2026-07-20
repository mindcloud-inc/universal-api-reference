# Stream: Search Channels

Finds channels in Stream by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/stream/latest/actions/search-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stream/latest/actions/search-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stream/latest/actions/search-channels?${params}`, {
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
| `filterConditions` | object | no | Channel query filter object. |
| `limit` | number | no | Maximum number of channels to return. |
| `offset` | number | no | Result offset for pagination. |
| `sort[]` | array<object> | no | Sort descriptors array. |
| `state` | boolean | no | Whether to include channel state. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": [
        {}
      ],
      "duration": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | array<object> |  |
| `duration` | string |  |

## Native endpoint

Through the native Stream API, this operation is `POST /channels` (base URL `https://chat.stream-io-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-channels.md) for the provider-specific parameters and requirements.

