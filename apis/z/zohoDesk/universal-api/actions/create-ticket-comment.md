# Zoho Desk: Create Ticket Comment



```
POST https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-ticket-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-ticket-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-ticket-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | The Zoho Desk ticket ID. |
| `content` | string | yes | Plain-text comment content to append to the ticket. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "commentedTime": "2026-05-07T12:00:00.000Z",
      "commenterId": "string",
      "content": "string",
      "contentType": "string",
      "encodedContent": "string",
      "id": "string",
      "isPublic": true,
      "modifiedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `commentedTime` | date |  |
| `commenterId` | string |  |
| `content` | string |  |
| `contentType` | string |  |
| `encodedContent` | string |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `modifiedTime` | date |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `POST /tickets/[:ticketId]/comments` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket-comment.md) for the provider-specific parameters and requirements.

