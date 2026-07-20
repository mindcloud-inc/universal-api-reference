# Pusher: List Channel Users

Retrieves users from a Pusher presence channel.

```
GET https://connect.mindcloud.co/v1/universal/pusher/latest/actions/list-channel-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pusher/latest/actions/list-channel-users?connectionId=$CONNECTION_ID&channelName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pusher/latest/actions/list-channel-users?${params}`, {
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
| `channelName` | string | yes | The presence channel whose subscribed user IDs you want to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "users": [
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
| `users` | array<object> | List of subscribed user ID objects for the presence channel. |

## Native endpoint

Through the native Pusher API, this operation is `GET /apps/{{credentials.appId}}/channels/:channel_name/users` (base URL `https://api-{{credentials.cluster}}.pusher.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-users.md) for the provider-specific parameters and requirements.

