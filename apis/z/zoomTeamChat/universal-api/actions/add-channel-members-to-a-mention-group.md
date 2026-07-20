# Zoom Team Chat: Add Channel Members To A Mention Group



```
PUT https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/add-channel-members-to-a-mention-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/add-channel-members-to-a-mention-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "mentionGroupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/add-channel-members-to-a-mention-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "mentionGroupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | The channel ID. |
| `mentionGroupId` | string | yes | The mention group ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoom Team Chat API returns.

## Native endpoint

Through the native Zoom Team Chat API, this operation is `POST /chat/channels/:channelId/mention_group/:mentionGroupId/members` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-channel-members-to-a-mention-group.md) for the provider-specific parameters and requirements.

