# Zoho Desk: List Ticket Comments



```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-ticket-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-ticket-comments?connectionId=$CONNECTION_ID&ticketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-ticket-comments?${params}`, {
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
| `ticketId` | string | yes | The Zoho Desk ticket ID. |

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

Through the native Zoho Desk API, this operation is `GET /tickets/[:ticketId]/comments` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-comments.md) for the provider-specific parameters and requirements.

