# Rocketlane: List Conversations

Lists conversations in Rocketlane.

```
GET https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-conversations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-conversations?${params}`, {
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
| `includeFields` | list<string> | no | Use this query parameter to opt in for fields to be returned in the response body. Use comma separated values to fetch the respective fields. If left blank, default properties are returned. |
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

Through the native Rocketlane API, this operation is `GET /1.0/conversations` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

