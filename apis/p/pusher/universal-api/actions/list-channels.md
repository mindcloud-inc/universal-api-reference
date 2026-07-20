# Pusher: List Channels

Retrieves channels from Pusher.

```
GET https://connect.mindcloud.co/v1/universal/pusher/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pusher/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pusher/latest/actions/list-channels?${params}`, {
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
| `filterByPrefix` | string | no | Return only channels whose names start with the provided prefix. |
| `info` | string | no | Comma-separated channel attributes to include in the response, such as user_count. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | object | Map of channel names to channel attribute objects. |

## Native endpoint

Through the native Pusher API, this operation is `GET /apps/{{credentials.appId}}/channels` (base URL `https://api-{{credentials.cluster}}.pusher.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

