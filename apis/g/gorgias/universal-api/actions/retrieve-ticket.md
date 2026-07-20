# Gorgias: Retrieve Ticket

Retrieves a ticket from Gorgias.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-ticket?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-ticket?${params}`, {
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
| `id` | string | yes | Ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee_team": {},
      "assignee_user": {},
      "channel": "string",
      "closed_datetime": "string",
      "created_datetime": "string",
      "custom_fields": {},
      "customer": {},
      "excerpt": "string",
      "external_id": "string",
      "from_agent": true,
      "id": 1,
      "integrations": [
        {}
      ],
      "is_unread": true,
      "language": "string",
      "last_message_datetime": "string",
      "last_received_message_datetime": "string",
      "last_sent_message_not_delivered": true,
      "messages_count": 1,
      "meta": {},
      "opened_datetime": "string",
      "priority": "string",
      "snooze_datetime": "string",
      "spam": true,
      "status": "string",
      "subject": "string",
      "summary": "string",
      "tags": [
        {}
      ],
      "trashed_datetime": "string",
      "updated_datetime": "string",
      "uri": "string",
      "via": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee_team` | object |  |
| `assignee_user` | object |  |
| `channel` | string |  |
| `closed_datetime` | string |  |
| `created_datetime` | string |  |
| `custom_fields` | object |  |
| `customer` | object |  |
| `excerpt` | string |  |
| `external_id` | string |  |
| `from_agent` | boolean |  |
| `id` | number |  |
| `integrations` | array<object> |  |
| `is_unread` | boolean |  |
| `language` | string |  |
| `last_message_datetime` | string |  |
| `last_received_message_datetime` | string |  |
| `last_sent_message_not_delivered` | boolean |  |
| `messages_count` | number |  |
| `meta` | object |  |
| `opened_datetime` | string |  |
| `priority` | string |  |
| `snooze_datetime` | string |  |
| `spam` | boolean |  |
| `status` | string |  |
| `subject` | string |  |
| `summary` | string |  |
| `tags` | array<object> |  |
| `trashed_datetime` | string |  |
| `updated_datetime` | string |  |
| `uri` | string |  |
| `via` | string |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /tickets/:id` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-ticket.md) for the provider-specific parameters and requirements.

