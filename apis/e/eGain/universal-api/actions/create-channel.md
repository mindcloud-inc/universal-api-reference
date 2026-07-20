# eGain: Create Channel

Creates a new channel in eGain.

```
POST https://connect.mindcloud.co/v1/universal/eGain/latest/actions/create-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGain/latest/actions/create-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "active": true,
  "description": "string",
  "displayName": "Ava Chen",
  "icon": "string",
  "restrictions.inbound.maxTextLength": 1,
  "restrictions.outbound.maxTextLength": 1,
  "restrictions.outbound.midChatAuth": true,
  "restrictions.outbound.systemMessages": true,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGain/latest/actions/create-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "active": true,
    "description": "string",
    "displayName": "Ava Chen",
    "icon": "string",
    "restrictions.inbound.maxTextLength": 1,
    "restrictions.outbound.maxTextLength": 1,
    "restrictions.outbound.midChatAuth": true,
    "restrictions.outbound.systemMessages": true,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | yes | Whether the channel is active. |
| `description` | string | yes | Channel description. |
| `displayName` | string | yes | Channel display name. |
| `icon` | string | yes | Base64 icon data. |
| `restrictions.inbound.maxTextLength` | number | yes | Maximum inbound text length. |
| `restrictions.outbound.maxTextLength` | number | yes | Maximum outbound text length. |
| `restrictions.outbound.midChatAuth` | boolean | yes | Whether mid-chat auth is enabled. |
| `restrictions.outbound.systemMessages` | boolean | yes | Whether outbound system messages are enabled. |
| `type` | string | yes | Channel type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eGain API returns.

## Native endpoint

Through the native eGain API, this operation is `POST /channels` (base URL `https://api.ai.egain.cloud/conversation/conversationmgr/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-channel.md) for the provider-specific parameters and requirements.

