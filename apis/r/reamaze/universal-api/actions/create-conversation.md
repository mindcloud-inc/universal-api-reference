# Reamaze: Create Conversation



```
POST https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/create-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversation": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/create-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversation": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversation` | object | yes | Body payload field documented on https://www.reamaze.com/api/post_conversations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": "string",
      "author": {},
      "category": {},
      "createdAt": "string",
      "data": {},
      "followers": [
        {}
      ],
      "lastCustomerMessage": {},
      "lastStaffMessage": {},
      "message": {},
      "slug": "string",
      "status": 1,
      "subject": "string",
      "tagList": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | string |  |
| `author` | object |  |
| `category` | object |  |
| `createdAt` | string |  |
| `data` | object |  |
| `followers` | array<object> |  |
| `lastCustomerMessage` | object |  |
| `lastStaffMessage` | object |  |
| `message` | object |  |
| `slug` | string |  |
| `status` | number |  |
| `subject` | string |  |
| `tagList` | array<string> |  |

## Native endpoint

Through the native Reamaze API, this operation is `POST /conversations` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversation.md) for the provider-specific parameters and requirements.

