# Freshdesk: List Ticket Conversations

Retrieves ticket conversations from Freshdesk by ticket ID.

```
GET https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/list-ticket-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/list-ticket-conversations?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/list-ticket-conversations?${params}`, {
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
| `id` | list<number> | yes | Freshdesk ticket ID. |

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

Through the native Freshdesk API, this operation is `GET /tickets/:id/conversations` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-conversations.md) for the provider-specific parameters and requirements.

