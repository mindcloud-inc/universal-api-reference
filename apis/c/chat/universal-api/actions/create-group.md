# 2Chat: Create Group

Creates a WhatsApp group in 2Chat.

```
POST https://connect.mindcloud.co/v1/universal/chat/latest/actions/create-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chat/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromNumber": "string",
  "group.name": "Ava Chen",
  "group.participants[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chat/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromNumber": "string",
    "group.name": "Ava Chen",
    "group.participants[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromNumber` | string | yes | The WhatsApp number connected to 2Chat that creates the group. |
| `group.name` | string | yes | The name of the WhatsApp group to create. |
| `group.description` | string | no | An optional description for the WhatsApp group. |
| `group.participants[]` | array<string> | yes | The phone numbers to add to the new WhatsApp group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 2Chat API returns.

## Native endpoint

Through the native 2Chat API, this operation is `POST /whatsapp/group/create` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group.md) for the provider-specific parameters and requirements.

