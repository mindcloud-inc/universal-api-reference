# Zoom Team Chat: List Members Of A Mention Group



```
GET https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-members-of-a-mention-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-members-of-a-mention-group?connectionId=$CONNECTION_ID&limit=25&offset=0&channelId=string&mentionGroupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "channelId": "string",
  "mentionGroupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-members-of-a-mention-group?${params}`, {
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
| `channelId` | string | yes | The channel ID. |
| `mentionGroupId` | string | yes | The mention group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "member_id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `member_id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Zoom Team Chat API, this operation is `GET /chat/channels/:channelId/mention_group/:mentionGroupId/members` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-members-of-a-mention-group.md) for the provider-specific parameters and requirements.

