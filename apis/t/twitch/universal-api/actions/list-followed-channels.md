# Twitch: List Followed Channels

Retrieves followed channels for a user from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-followed-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-followed-channels?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-followed-channels?${params}`, {
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
| `userId` | string | yes | Returns broadcasters followed by this user. This ID must match the user ID in the user OAuth token. |
| `broadcasterId` | string | no | Filters the response to a specific broadcaster to check whether the user follows them. |
| `first` | number | no | Maximum number of followed channels to return. Minimum 1, maximum 100. |
| `after` | string | no | Cursor for the next page of followed channels. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "broadcasterId": "string",
      "broadcasterLogin": "string",
      "broadcasterName": "Ava Chen",
      "followedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcasterId` | string |  |
| `broadcasterLogin` | string |  |
| `broadcasterName` | string |  |
| `followedAt` | string |  |

## Native endpoint

Through the native Twitch API, this operation is `GET /channels/followed` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-followed-channels.md) for the provider-specific parameters and requirements.

