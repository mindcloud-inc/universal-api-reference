# Freshdesk: Create Reply

Creates a reply to a Freshdesk ticket.

```
POST https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-reply
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-reply" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-reply', {
  method: 'POST',
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
| `id` | list<number> | yes | Freshdesk ticket ID. |
| `body` | string | no | Reply content in HTML |
| `structuredBody` | object | no | Structured content body for the reply |
| `attachments[]` | array<object> | no | Reply attachments |
| `fromEmail` | string | no | Email address from which the reply is sent |
| `userId` | list<number> | no | Agent user ID adding the reply |
| `ccEmails[]` | array<string> | no | CC recipients for the outgoing reply |
| `bccEmails[]` | array<string> | no | BCC recipients for the outgoing reply |

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
| `ticketId` | number |  |
| `toEmails` | array<string> |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Freshdesk API, this operation is `POST /tickets/:id/reply` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reply.md) for the provider-specific parameters and requirements.

