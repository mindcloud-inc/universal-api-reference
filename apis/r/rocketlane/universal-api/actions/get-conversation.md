# Rocketlane: Get Conversation

Retrieves a conversation from Rocketlane.

```
GET https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/get-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/get-conversation?connectionId=$CONNECTION_ID&conversationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/get-conversation?${params}`, {
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
| `conversationId` | number | yes | The ID of the conversation object |
| `includeFields` | list<string> | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | boolean | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |

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

Through the native Rocketlane API, this operation is `GET /1.0/conversations/:conversationId` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation.md) for the provider-specific parameters and requirements.

