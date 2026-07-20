# 2Chat: Add Participant

Updates a WhatsApp group in 2Chat by adding participants.

```
PUT https://connect.mindcloud.co/v1/universal/chat/latest/actions/add-participant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chat/latest/actions/add-participant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group_uuid": "string",
  "fromNumber": "string",
  "participants[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chat/latest/actions/add-participant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group_uuid": "string",
    "fromNumber": "string",
    "participants[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `group_uuid` | string | yes | The UUID of the WhatsApp group. |
| `fromNumber` | string | yes | The WhatsApp number connected to 2Chat that adds participants. |
| `participants[]` | array<string> | yes | The phone numbers to add to the group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 2Chat API returns.

## Native endpoint

Through the native 2Chat API, this operation is `POST /whatsapp/group/:group_uuid/add-participant` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-participant.md) for the provider-specific parameters and requirements.

