# Twitch: List Chatters

Retrieves channel chatter records from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-chatters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-chatters?connectionId=$CONNECTION_ID&limit=25&offset=0&broadcasterId=string&moderatorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "broadcasterId": "string",
  "moderatorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-chatters?${params}`, {
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
| `broadcasterId` | string | yes | ID of the broadcaster whose chatters you want to list. |
| `moderatorId` | string | yes | ID of the moderator or broadcaster making the request. Must match the user in the OAuth token. |
| `limit` | number | no | Maximum number of chatters to return. Minimum 1, maximum 1,000. |
| `cursor` | string | no | Cursor for forward pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
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
| `data` | array<object> | Chatter rows. |
| `data[].userId` | string | Chatter user identifier. |
| `data[].userLogin` | string | Chatter login name. |
| `data[].userName` | string | Chatter display name. |
| `pagination` | object | Pagination cursor payload. |
| `pagination.cursor` | string | Cursor for the next page of results. |
| `total` | number | Total number of connected chatters. |

## Native endpoint

Through the native Twitch API, this operation is `GET /chat/chatters` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-chatters.md) for the provider-specific parameters and requirements.

