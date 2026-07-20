# Intercom: Reply Ticket



```
PUT https://connect.mindcloud.co/v1/universal/intercom/latest/actions/reply-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/reply-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "string",
  "admin_id": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intercom/latest/actions/reply-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "string",
    "admin_id": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | Intercom ticket identifier |
| `admin_id` | string | yes | Admin sending the reply |
| `body` | string | yes | Reply content |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appPackageCode": "string",
      "attachments": [
        "string"
      ],
      "author": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "body": "string",
      "createdAt": 1,
      "id": "string",
      "partType": "string",
      "redacted": true,
      "type": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appPackageCode` | string |  |
| `attachments` | array<string> |  |
| `author` | object |  |
| `author.email` | string |  |
| `author.id` | string |  |
| `author.name` | string |  |
| `author.type` | string |  |
| `body` | string |  |
| `createdAt` | number |  |
| `id` | string |  |
| `partType` | string |  |
| `redacted` | boolean |  |
| `type` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Intercom API, this operation is `POST /tickets/:ticket_id/reply` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reply-ticket.md) for the provider-specific parameters and requirements.

