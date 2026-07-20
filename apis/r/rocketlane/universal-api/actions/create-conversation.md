# Rocketlane: Create Conversation

Creates a conversation in Rocketlane.

```
POST https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/create-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "source": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/create-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "source": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeFields` | list<string> | no | Use this query parameter to opt in for fields to be returned in the response body. Use comma separated values to fetch the respective fields. If left blank, default properties are returned. |
| `includeAllFields` | boolean | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `name` | string | yes | Conversation name |
| `description` | string | no | Conversation description |
| `source` | object | yes | Source associated with the conversation |
| `allMembers` | boolean | no | Conversation all members inclusion |
| `members` | list<object> | no | Conversation members |
| `private` | boolean | no | Conversation privacy |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allMembers": true,
      "conversationId": 1,
      "conversationName": "Ava Chen",
      "createdAt": 1,
      "description": "string",
      "members": [
        {}
      ],
      "private": true,
      "source": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allMembers` | boolean | Conversation all members inclusion |
| `conversationId` | number | Conversation ID |
| `conversationName` | string | Conversation name |
| `createdAt` | number | Conversation Created timestamp |
| `description` | string | Conversation description |
| `members` | array<object> | Conversation members |
| `private` | boolean | Conversation privacy |
| `source` | object | Source associated with the conversation |

## Native endpoint

Through the native Rocketlane API, this operation is `POST /1.0/conversations` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversation.md) for the provider-specific parameters and requirements.

