# Zendesk: List Ticket Comments

Retrieves comments for a Zendesk ticket.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-ticket-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-ticket-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&ticket_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "ticket_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-ticket-comments?${params}`, {
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
| `ticket_id` | number | yes | Zendesk ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "authorId": 1,
      "body": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "htmlBody": "string",
      "id": 1,
      "plainBody": "string",
      "public": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments[]` | object | Comment attachment objects. |
| `authorId` | number | Author user id. |
| `body` | string | Ticket comment body. |
| `createdAt` | date | Creation timestamp. |
| `htmlBody` | string | HTML version of the comment body. |
| `id` | number | Ticket comment id. |
| `plainBody` | string | Plain-text version of the comment body. |
| `public` | boolean | Whether the comment is public. |
| `type` | string | Ticket comment type. |

## Native endpoint

Through the native Zendesk API, this operation is `GET /tickets/:ticket_id/comments.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ticket-comments.md) for the provider-specific parameters and requirements.

