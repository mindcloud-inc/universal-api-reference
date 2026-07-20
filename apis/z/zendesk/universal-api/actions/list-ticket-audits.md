# Zendesk: List Ticket Audits

Retrieves audits for a Zendesk ticket.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-ticket-audits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-ticket-audits?connectionId=$CONNECTION_ID&limit=25&offset=0&ticket_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "ticket_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-ticket-audits?${params}`, {
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
      "authorId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "events": [
        {}
      ],
      "id": 1,
      "ticketId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | number | Author user id for the audit. |
| `createdAt` | date | Audit creation timestamp. |
| `events[]` | object | Audit event objects. |
| `id` | number | Ticket audit id. |
| `ticketId` | number | Ticket id for the audit. |

## Native endpoint

Through the native Zendesk API, this operation is `GET /tickets/:ticket_id/audits.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ticket-audits.md) for the provider-specific parameters and requirements.

