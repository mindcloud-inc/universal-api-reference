# Rocketlane: Remove Conversation Members

Removes members from a conversation in Rocketlane.

```
PUT https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/remove-conversation-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/remove-conversation-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/remove-conversation-members', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | number | yes | The ID of the conversation object |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversationId": 1,
      "members": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversationId` | number | Conversation ID |
| `members` | array<object> | Conversation Members |

## Native endpoint

Through the native Rocketlane API, this operation is `POST /1.0/conversations/:conversationId/remove-members` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-conversation-members.md) for the provider-specific parameters and requirements.

