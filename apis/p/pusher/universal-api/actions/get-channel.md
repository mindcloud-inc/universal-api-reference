# Pusher: Get Channel

Retrieves channel details from Pusher.

```
GET https://connect.mindcloud.co/v1/universal/pusher/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pusher/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pusher/latest/actions/get-channel?${params}`, {
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
| `channelName` | string | yes | The name of the channel to inspect. |
| `info` | string | no | Comma-separated channel attributes to include, such as user_count or subscription_count. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cache": {},
      "occupied": true,
      "subscription_count": 1,
      "user_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cache` | object | Cache payload and TTL for cache channels when requested. |
| `occupied` | boolean | Whether the channel currently has any subscribers. |
| `subscription_count` | number | Subscribed connections for supported channel types when requested. |
| `user_count` | number | Distinct subscribed users for presence channels when requested. |

## Native endpoint

Through the native Pusher API, this operation is `GET /apps/{{credentials.appId}}/channels/:channel_name` (base URL `https://api-{{credentials.cluster}}.pusher.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.

