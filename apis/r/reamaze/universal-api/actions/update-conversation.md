# Reamaze: Update Conversation



```
PUT https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/update-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/update-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/update-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | yes | Path parameter for slug. |
| `conversation` | object | no | Body payload field documented on https://www.reamaze.com/api/put_conversations. |

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

Through the native Reamaze API, this operation is `PUT /conversations/:slug` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation.md) for the provider-specific parameters and requirements.

