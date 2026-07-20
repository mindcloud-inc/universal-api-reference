# WotNot: Start API Channel Conversation

Creates an API channel conversation in WotNot.

```
POST https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/start-api-channel-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/start-api-channel-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message.data.body": "string",
  "publish_key": "string",
  "from.user_external_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/start-api-channel-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message.data.body": "string",
    "publish_key": "string",
    "from.user_external_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message.data.body` | string | yes | Initial visitor message |
| `publish_key` | string | yes | API-channel publish key from the API bot |
| `from.user_external_id` | string | yes | Unique visitor ID from your system |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WotNot API returns.

## Native endpoint

Through the native WotNot API, this operation is `POST /api/v1/conversations` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-api-channel-conversation.md) for the provider-specific parameters and requirements.

