# Freshdesk: Update Conversation

Updates an existing conversation in Freshdesk.

```
PUT https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/update-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/update-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/update-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Freshdesk conversation ID. |
| `attachments[]` | array<object> | no | Conversation attachments |
| `body` | string | no | Updated conversation content in HTML |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "body": "string",
      "bodyText": "string",
      "createdAt": "string",
      "id": 1,
      "incoming": true,
      "private": true,
      "ticketId": 1,
      "toEmails": [
        "ava@example.com"
      ],
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `body` | string |  |
| `bodyText` | string |  |
| `createdAt` | string |  |
| `id` | number |  |
| `incoming` | boolean |  |
| `private` | boolean |  |
| `ticketId` | number |  |
| `toEmails` | array<string> |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Freshdesk API, this operation is `PUT /conversations/:id` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation.md) for the provider-specific parameters and requirements.

