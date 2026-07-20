# Twitch: List Channel Followers

Retrieves channel follower records from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-channel-followers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-channel-followers?connectionId=$CONNECTION_ID&limit=25&offset=0&broadcasterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "broadcasterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-channel-followers?${params}`, {
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
| `broadcasterId` | string | yes | The broadcaster’s ID. |
| `userId` | string | no | A user’s ID used to check whether they follow the broadcaster. |
| `first` | number | no | The maximum number of items to return per page. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | string | no | The cursor used to get the next page of results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "followedAt": "string",
          "userId": "string",
          "userLogin": "string",
          "userName": "Ava Chen"
        }
      ],
      "pagination": {
        "cursor": "string"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Follower rows. |
| `data[].followedAt` | string | Timestamp when the user followed the broadcaster. |
| `data[].userId` | string | Follower user identifier. |
| `data[].userLogin` | string | Follower login name. |
| `data[].userName` | string | Follower display name. |
| `pagination` | object | Pagination cursor payload. |
| `pagination.cursor` | string | Cursor for the next page of results. |
| `total` | number | Total number of followers. |

## Native endpoint

Through the native Twitch API, this operation is `GET /channels/followers` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channel-followers.md) for the provider-specific parameters and requirements.

