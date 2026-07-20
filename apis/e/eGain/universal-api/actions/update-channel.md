# eGain: Update Channel

Updates an existing channel in eGain.

```
PUT https://connect.mindcloud.co/v1/universal/eGain/latest/actions/update-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eGain/latest/actions/update-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "active": true,
  "description": "string",
  "displayName": "Ava Chen",
  "icon": "string",
  "id": "string",
  "restrictions.inbound.maxTextLength": 1,
  "restrictions.outbound.maxTextLength": 1,
  "restrictions.outbound.midChatAuth": true,
  "restrictions.outbound.systemMessages": true,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGain/latest/actions/update-channel', {
  method: 'PUT',
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
    "id": "string",
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
| `active` | boolean | yes | Whether channel is active. |
| `description` | string | yes | Channel description. |
| `displayName` | string | yes | Channel display name. |
| `icon` | string | yes | Channel icon. |
| `id` | string | yes | Channel ID. |
| `restrictions.inbound.maxTextLength` | number | yes | Inbound max text length. |
| `restrictions.outbound.maxTextLength` | number | yes | Outbound max text length. |
| `restrictions.outbound.midChatAuth` | boolean | yes | Whether mid chat auth is enabled. |
| `restrictions.outbound.systemMessages` | boolean | yes | Whether system messages are enabled. |
| `type` | string | yes | Channel type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eGain API returns.

## Native endpoint

Through the native eGain API, this operation is `PUT /channels/:id` (base URL `https://api.ai.egain.cloud/conversation/conversationmgr/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-channel.md) for the provider-specific parameters and requirements.

